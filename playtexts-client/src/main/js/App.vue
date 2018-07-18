<template>
  <div id="app" class="playtexts-wrapper">
    <PlaytextsHeader />
    <PlaytextsBanner v-if="false" />
    <div class="content-wrapper">
      <div class="content-flex-area">
        <main class="content-main"><router-view /></main>
        <PlaytextsNavigation />
        <PlaytextsNotifications />
      </div>
    </div>
    <PlaytextsFooter />
  </div>
</template>

<script>
import PlaytextsHeader from './components/PlaytextsHeader.vue'
import PlaytextsBanner from './components/PlaytextsBanner.vue'
import PlaytextsNavigation from './components/PlaytextsNavigation.vue'
import PlaytextsNotifications from './components/PlaytextsNotifications.vue'
import PlaytextsFooter from './components/PlaytextsFooter.vue'

export default {
  components: {
    PlaytextsHeader,
    PlaytextsBanner,
    PlaytextsNavigation,
    PlaytextsNotifications,
    PlaytextsFooter,
  },
}
</script>

<style lang="stylus">
@import './styles/main.styl';

.playtexts-wrapper
  margin 0
  padding 0

.content-wrapper
  min-width $page-size
  min-height 100px
  display flex
  flex-direction column

  .content-flex-area
    display flex
    flex 0

    .content-main
      flex 1

</style>
