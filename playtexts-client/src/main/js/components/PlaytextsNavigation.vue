<template>
  <nav class="content-navigation">
    <router-link
      v-for="entry of navEntries"
      class="link"
      :key="entry.id"
      :to="{ name: entry.route }">
      {{ entry.label }}
    </router-link>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      navEntries: [],
    }
  },

  created () {
    this.navEntries = [
      {
        id: 1,
        name: 'viewer',
        label: 'Viewer',
        route: 'factsheets',
      },
      {
        id: 2,
        name: 'editor',
        label: 'Editor',
        route: 'editor',
      },
    ]
  },
}
</script>

<style lang="stylus" scoped>
@import "../styles/imports.styl"
.content-navigation
  padding 5px
  flex: 0 0 20em;
  order -1

  a
    color black
    display block
    min-height 20px
    border 1px $md-amber-400
    background-color $md-amber-100
    padding 8px 12px
    margin 3px
    box-shadow 2px 2px 2px 0px rgba(0,0,0,0.25)

    &:hover
      box-shadow none

</style>
