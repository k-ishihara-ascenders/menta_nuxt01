<template>
  <div>
    <sample-component :title="indexTitle">
      <div class="come">slot example</div>
      <div slot="named">秦基博</div>
    </sample-component>

    <nuxt-link to="/about">ABOUT</nuxt-link>
  </div>
</template>

<script>
import SampleComponent from '~/components/SampleComponent.vue'

export default {
  components: {
    SampleComponent,
  },
  data() {
    return {
      indexTitle: '星野源',
    }
  },
}
</script>

<style></style>
