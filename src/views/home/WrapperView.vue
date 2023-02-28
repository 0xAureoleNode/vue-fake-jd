<template>
  <div class="wrapper">
    <StaticPartView />
    <NearByView />
  </div>
</template>

<script>
import StaticPartView from './StaticPartView.vue'
import NearByView from './NearByView.vue'
export default {
  components: { StaticPartView, NearByView },
  name: 'WrapperView',
}
</script>

<style lang="scss" scoped>
.wrapper {
  overflow-y: auto;
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0.5rem;
  right: 0;
  padding: 0 0.18rem 0.1rem 0.18rem;
}
</style>
