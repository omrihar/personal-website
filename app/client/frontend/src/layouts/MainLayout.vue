<template lang="pug">
q-layout(id="main")
  q-layout-header.no-shadow
    .row.q-pa-xl
      .col-8
      .col-4
        .navContainer
          q-btn.text-weight-thin(to="/" label="About" flat size='xl')
          q-btn.text-weight-thin(label="Projects" flat size='xl')
          q-btn.text-weight-thin(label="CV" flat size='xl')
          q-btn.text-weight-thin(label="Concepts" flat size='xl')
          q-btn.text-weight-thin(label="etc" flat size='xl')

  q-layout-footer

  //-q-layout-drawer(side="left", v-model="leftDrawer", color="secondary")
    //-o-drawer

  q-page-container
    router-view
</template>

<script>

import ODrawer from '../components/ODrawer.vue'

export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawer: true
    }
  },

  components: {
    ODrawer
  }
}
</script>

<style lang="stylus">
@import '~variables'
#main
   background-color: $secondary

.navContainer
  /*border: 3px solid $primary*/
  /*border-radius: 5px*/
  padding 10px
  /*width: 75%*/
  /*background-color: $tertiary*/
</style>
