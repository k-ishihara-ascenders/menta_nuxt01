<template lang="html">
  <nuxt-link to="/">TOP</nuxt-link>
</template>

<script>
export default {
  head() {
    return {
      title: 'About',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Aboutページ',
        },
      ],
    }
  },
  layout: 'dark',
}
</script>

<style lang="css" scoped></style>
