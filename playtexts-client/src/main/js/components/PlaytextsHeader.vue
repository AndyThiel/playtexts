<template>
  <header class="faf-header">
    <div class="content">
      <router-link class="link" :to="{ name: 'home' }"><h1 v-html="fafTitle"></h1></router-link>
    </div>
    <div class="header-quick-navigation">
      <QuickNavigation />
    </div>
  </header>
</template>

<script>
import QuickNavigation from './QuickNavigation'

export default {
  components: {
    QuickNavigation,
  },

  data () {
    return {
      fafTitle: null,
    }
  },

  mounted () {
    this.fafTitle = 'FactsAreFun.com'
  },
}
</script>

<style lang="stylus" scoped>
@import "../styles/vars"

.faf-header
  font-family sans-serif
  text-align left
  box-shadow 4px 4px 3px 0px rgba(0,0,0,0.25)
  position relative

  .content
    max-width $page-size
    margin 0
    padding 10px
    box-sizing border-box
    position relative
    height 75px

   a
     h1
       color: $color-accent2
       font-size 1.5em

</style>
