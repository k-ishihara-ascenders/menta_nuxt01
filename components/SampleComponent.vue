<template lang="html">
  <div>
    <h1>{{ title }}</h1>
    <p>Hello, {{ name }} {{ reverseName }}</p>
    <button type="button" name="button" @click="plus">
      click times: {{ num }}
    </button>

    <div :class="['hide', { seven: num === 7 }]">7times</div>

    <div class="slot">
      <slot />
    </div>

    <div>
      <slot name="named" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default Title',
    },
  },
  data() {
    return {
      name: 'Ken',
      num: 0,
    }
  },
  computed: {
    reverseName() {
      return this.name.split('').reverse().join('')
    },
  },
  mounted() {
    console.log('ちんこ')
  },
  methods: {
    plus() {
      this.num++
    },
  },
}
</script>

<style lang="scss" scoped>
.hide {
  display: none;

  &.seven {
    display: block;
  }
}
.slot {
  color: red;
}
</style>
