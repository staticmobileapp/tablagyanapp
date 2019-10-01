<template>
    <div class="videoPlayer">
        <iframe autoplay :src="video"></iframe>
    </div>
</template>

<script>
export default {
    name: "Player",
    props: ['item'],
    computed: {
        video() {
            return `https://www.youtube.com/embed/${this.item.videoId}`
        }
    },
}
</script>

<style lang="scss">
.videoPlayer {
    margin:0 0;
    padding: 0 0;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    z-index: 99999;
    iframe {
        width: 100%;
        background-color: #000;
        height: 300px;
    }
}
</style>
