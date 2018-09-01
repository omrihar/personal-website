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
    .mystyle
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

.mystyle
  background-color: white
  max-width: 100rem
  min-height: 40rem
  margin: 0 auto
  padding: 5rem

p
  font-size: 28px
  padding: 1rem

p a
  color: green
  text-decoration: none

.mystyle p a:hover
  text-decoration: underline

</style>
