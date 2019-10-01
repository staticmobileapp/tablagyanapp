<template>
    <div ref="setActiveVideo" id="videolist">
        <template v-if="vList && vList.length > 0">
            <player :item="activeVideo"  />
            <list :itemList="vList" @changeVideoitem="setVideoitem" />
        </template>
        <template v-else>
            <h2>Please pass list array to videoListing component</h2>
        </template>
    </div>
</template>

<script>
import List from './List';
import Player from './Player';
export default {
    name: "ListingContent",
    //props: ['vList'],
    components: {
        List,
        Player
    },
    data() {
        return {
            activeVideo: {},
            vList: [
                {
                    videoId:"ZelGEue9Yyw",
                    title: "TablaGyan Academy of Music - Intro video",
                    description: "TablaGyan Academy of Music - Intro video"
                },
                {
                    videoId:"41KYrhgX2RQ",
                    title: "Guruji’s Concert",
                    description: "Guruji’s Concert"
                },
                {
                    videoId:"CZV4VTliaec",
                    title: "Guruji’s Concert",
                    description: "Guruji’s Concert"
                },
                {
                    videoId:"xMtH3rntsEA",
                    title: "Special Performance By Pandit Krishnendra Wadikar and Sri Satish Kolli",
                    description: "Special Performance By Pandit Krishnendra Wadikar and Sri Satish Kolli"
                },
                {
                    videoId:"r15_6z9xryo",
                    title: "Inside The World's Only Private Boeing 787 Dreamliner!",
                    description: ""
                },
                {
                    videoId:"nta-Rv7sqcQ",
                    title: "TablaGyan - Guru Poornima 2017 - Part 2",
                    description: "TablaGyan - Guru Poornima 2017 - Part 2"
                },
                {
                    videoId:"VOVFYOJOkI4",
                    title: "jugalbandi sitar violin tabla TablaGyan - informal medley -Sitar, Violin and Tabla.",
                    description: "jugalbandi sitar violin tabla TablaGyan - informal medley -Sitar, Violin and Tabla."
                },
                {
                    videoId:"SYvots12qk0",
                    title: "Delhi kaida TeenTaal",
                    description: "Delhi kaida TeenTaal"
                },
                {
                    videoId:"hmpCG0AnUz4",
                    title: "Rela TeenTaal",
                    description: "Rela TeenTaal"
                }
            ]
        }
    },
    mounted () {
        this.activeVideo = this.setVideoitem();
    },
    methods: {
        setVideoitem(item="") {
            if(item == '') {
                return this.vList[0]
            } else {
                return this.activeVideo = item
            }

        }
    },
}
</script>

<style scoped>
#videolist {
  top: 500px;
  position: absolute;
}
</style>
