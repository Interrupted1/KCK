<template>
  <div id="app">
    <component :is="layout">
      <router-view></router-view>
    </component>
  </div>
</template>

<script>
var default_layout = "Default"
export default {
  computed: {
    layout() {
      return (this.$route.meta.layout || default_layout) + '-layout'
    }
  }
}
</script>
