<template>
  <div class="list row">
      <list-item v-for="(item, index) in itemList" :itemDetail="item" :key="index" class="customCard col-lg-3 col-md-4 col-sm-6 col-6" @changeItem="changeVideoitem"
      />
  </div>
</template>

<script>
import ListItem from './ListItem'
export default {
  name: 'List',
  components: {
    ListItem
  },
  props: ['item-list'],
  methods: {
    changeVideoitem (id) {
      this.$emit('changeVideoitem', id)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.list {
  padding: 15px 0px;
}
</style>
