<template lang="pug">
q-page
  vue-markdown(:breaks="false").
    I'm **Omri Har-Shemesh**, a father, a physicist, a data scientist and
    a developer.

    I've studied [strong lasers](1) as a **physicist**, [phase](2)
    [transitions](3) in complex systems as a **computational scientist** and
    cognitive development, human psychology, diplomacy and sleep deprivation
    as a **father**.

    An enthusiastic python developer, I have a love-hate relationship with
    JavaScript (though [`Vue.js`]() is awesome) and love to tinker with data
    visualizations using `matplotlib`, `plotly`, `d3.js` and `chart.js`.

    Originally from **Israel**, I live now in **Bonn, Germany** and
    juggle Hebrew, German and English in my daily life.

    $$ E = mc^2 $$

</template>

<script>
import VueMarkdown from 'vue-markdown'

export default {
  name: 'About',

  mounted () {
    window.Prism.highlightAll()
  },

  components: {
    VueMarkdown
  }
}
</script>

<style lang="stylus">
</style>
