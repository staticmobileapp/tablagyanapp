<template>
  <q-page padding id="app">
    <ListingContent />
    <ul>
      <li v-for="(video,index) in videolist" :key="index">{{video.title}}</li>
    </ul>
  </q-page>
</template>

<style>
.logo-center {
width: 10%;
height: 10%;
}
#app {
  background-image: linear-gradient(to bottom, #5939b0, #5335a5, #4d319a, #482d8f, #422984, #3b2579, #35226e, #2f1e63, #271a55, #201548, #19113b, #140a2e);
  min-height: 500px;
  color: #ffffff;
}

</style>

<script>
import ListingContent from '../components/ListingContent.vue';

export default {
  name: 'PageIndex',
  components: {
       ListingContent
    },
  data() {
    return {
      videolist: [
        {title: "TablaGyan Academy of Music - Intro video", link: "https://www.youtube.com/watch?v=ZelGEue9Yyw"},
        {title: "Guruji’s Concert", link: "https://www.youtube.com/watch?v=41KYrhgX2RQ"},
        {title: "Guruji’s Concert", link: "https://www.youtube.com/watch?v=CZV4VTliaec"},
        {title: "Special Performance By Pandit Krishnendra Wadikar and Sri Satish Kolli", link: "https://www.youtube.com/watch?v=xMtH3rntsEA"},
        {title: "TablaGyan - Guru Poornima 2017 - Part 2", link: "https://www.youtube.com/watch?v=nta-Rv7sqcQ"},
        {title: "jugalbandi sitar violin tabla TablaGyan - informal medley -Sitar, Violin and Tabla.", link: "https://www.youtube.com/watch?v=VOVFYOJOkI4"},
        {title: "Delhi kaida TeenTaal", link: "https://www.youtube.com/watch?v=SYvots12qk0"},
        {title: "Rela TeenTaal", link: "https://www.youtube.com/watch?v=hmpCG0AnUz4"}
      ]
    }
  }
}
</script>
