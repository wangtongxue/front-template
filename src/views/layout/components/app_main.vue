<template>
  <section class="app-main">
    <transition name="fade" mode="out-in">
      <keep-alive :include="cachedViews">
        <router-view></router-view>
      </keep-alive>
    </transition>
  </section>
</template>

<script>
export default {
  name: 'AppMain',
  computed: {
    cachedViews () {
      return [] // read from state
    }
  }
}
</script>

<style scoped lang="less">
.app-main {
  min-height: 100%;
}
</style>
