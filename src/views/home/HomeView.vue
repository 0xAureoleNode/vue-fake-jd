<template>
  <div>
    <WrapperViewVue />
    <DockerViewVue />
  </div>
</template>
<script>
import DockerViewVue from './DockerView.vue'
import WrapperViewVue from './WrapperView.vue'
export default {
  components: { WrapperViewVue, DockerViewVue },
  name: 'Home',
}
</script>
