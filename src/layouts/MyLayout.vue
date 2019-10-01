<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
        >
          <q-icon name="menu" />
        </q-btn>

        <q-toolbar-title>
          TablaGyan
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
      content-class="bg-grey-2"
    >
      <q-list>
        <q-item-label header>Navigation</q-item-label>
        <q-item clickable to="/" exact>
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Home</q-item-label>
          </q-item-section>
        </q-item>


        <q-item clickable to="/about" exact>
          <q-item-section avatar>
            <q-icon name="info" />
          </q-item-section>
          <q-item-section>
            <q-item-label>About us</q-item-label>
          </q-item-section>
        </q-item>
         <q-item clickable to="/videos" exact>
          <q-item-section avatar>
            <q-icon name="videocam" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Event recordings</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://www.facebook.com/TablaGyanschooloftabla/">
          <q-item-section avatar>
            <q-icon name="public" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Facebook</q-item-label>
            <q-item-label caption>@TablaGyanschooloftabla</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://www.youtube.com/channel/UCPs6c3nl-pkl_q5S20x_qWg">
          <q-item-section avatar>
            <q-icon name="video_library" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Videos</q-item-label>
            <q-item-label caption>Youtube channel</q-item-label>
          </q-item-section>
        </q-item>
         <q-item clickable tag="a" target="_blank" href="http://www.tablagyan.com/html/classes.php">
          <q-item-section avatar>
            <q-icon name="school" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Website</q-item-label>
            <q-item-label caption>www.tablagyan.com</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
      leftDrawerOpen: this.$q.platform.is.desktop
    }
  },
  methods: {
    openURL
  }
}
</script>

<style>
</style>
