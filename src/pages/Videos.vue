<template>
  <q-page padding>
    <ul>
      <li v-for="video in videolist">{{video.title}}</li>
      <li v-for="(index,video) in videolist" :key="index">{{video.title}}</li>
    </ul>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'Videos',
  data() {
    return {
      videolist: [
        {"title": "TablaGyan Academy of Music - Intro video", "link": "https://www.youtube.com/watch?v=ZelGEue9Yyw"},
        {"title": "Guruji’s Concert", "link": "https://www.youtube.com/watch?v=41KYrhgX2RQ"},
        {"title": "Guruji’s Concert", "link": "https://www.youtube.com/watch?v=CZV4VTliaec"},
        {"title": "Special Performance By Pandit Krishnendra Wadikar and Sri Satish Kolli", "link": "https://www.youtube.com/watch?v=xMtH3rntsEA"},
        {"title": "TablaGyan - Guru Poornima 2017 - Part 2", "link": "https://www.youtube.com/watch?v=nta-Rv7sqcQ"},
        {"title": "jugalbandi sitar violin tabla TablaGyan - informal medley -Sitar, Violin and Tabla.", "link": "https://www.youtube.com/watch?v=VOVFYOJOkI4"},
        {"title": "Delhi kaida TeenTaal", "link": "https://www.youtube.com/watch?v=SYvots12qk0"},
        {"title": "Rela TeenTaal", "link": "https://www.youtube.com/watch?v=hmpCG0AnUz4"}
      ]
    }
  }
}
</script>
