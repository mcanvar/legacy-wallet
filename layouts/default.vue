<template>
  <div>
    <theme-navbar />

    <Nuxt />

    <theme-footer />

    <dialog-modal />

    <cookie-box />
  </div>
</template>

<script>
import storage from '@/mixins/storage'

export default {
  mixins: [storage],
  head() {
    return {
      titleTemplate: this.$t('title_template'),
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.$t('meta_description'),
        },
      ],
    }
  },
}
</script>
