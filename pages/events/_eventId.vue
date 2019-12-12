<template>
    <div>
        <div class="header">
            <div class="gradient">
                <el-row type="flex" justify="center">
                    <el-col :xs="22" :sm="22" :md="22" :lg="20" :xl="18">
                        <div class="breadcrumb">
                            <h3>{{ event.fields.title }}</h3> <p>{{ startDate }} - {{ endDate}}</p>
                        </div>
                    </el-col>
                </el-row>
            </div>
        </div>
        <div class="event-content" :key="$route.fullPath">
            <div class="image">
                <event-banner-image :src="bannerUrl" />
            </div>

            <div class="description">
                <h3> Overview </h3>
                <p>{{ event.fields.description }}</p>
            </div>
        </div>

        <div class="section">
            {{event.fields}}
        </div>
    </div>
</template>

<script>
    import createClient from '@/plugins/contentful.js'
    import { format, formatDistance, formatRelative, subDays, parseISO } from 'date-fns'
    import eventBannerImage from '@/components/EventBannerImage/EventBannerImage.vue'


    const client = createClient()

    export default {
        name: 'event-detail',

        components: {
            eventBannerImage
        },

        computed: {
            bannerUrl: function () {
                try {
                    return this.event.fields.image.fields.file.url
                }
                catch {
                    console.log(this.event.fields)
                }
            },
            startDate: function() {
                return format(parseISO(this.event.fields.startDate),'MM/dd/yyyy')
            },
            endDate: function() {
                return format(parseISO(this.event.fields.endDate),'MM/dd/yyyy')
            }
        },

        asyncData (env) {
            return Promise.all([
                // fetch all blog posts sorted by creation date
                client.getEntry(env.params.eventId)
            ]).then(([events]) => {
                // return data that should be available
                // in the template
                return {
                event: events
                }
            }).catch(console.error)
        }
    }

</script>

<style lang="scss" scoped>
@import '@/assets/_variables.scss';
.header {
  .gradient {
    padding: 1.5em 0;
    color: #f0f2f5;
    background-image: linear-gradient(90deg, #0026ff 0%, #00ffb9 100%);

    .breadcrumb {
      width: 75%;
    }
  }
}

.event-content {
    display: flex;
    flex-direction: row;
    padding: 24px 16px;
    img {
        display: block;
        width: 200px;
        height: 200px;
    }

    h3: {
        margin-bottom: 8px;
    }

    .image {
        margin: 16px;
    }

    .description {
            max-width: 600px;
        }
    
    .event-content-wrap {
        margin-left: 16px;
    }
}

</style>