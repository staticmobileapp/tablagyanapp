<template>
    <div class="row items-start ">
        <q-card class="my-card"
            @click="changeVideo(itemDetail)"
        >
        <img :src="getImageUrl">
            <q-card-section>
               <div class="text-h6">
                {{ itemDetail.description }}
                </div>
            </q-card-section>
        </q-card>
    </div>
</template>

<script>
export default {
    name: "ListItem",
    props:['item-detail'],
    computed: {
        getImageUrl() {
            return `https://img.youtube.com/vi/${this.itemDetail.videoId}/0.jpg`
        }
    },
    methods: {
        changeVideo(item) {
            this.$emit('changeItem', item)
        }
    },
}
</script>

<style  lang="scss" scoped>
.my-card {
  width: 100%;
  max-width: 100%;
  }
</style>
