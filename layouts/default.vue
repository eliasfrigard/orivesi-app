<template>
  <div>
    <NavigationTop />
    <Nuxt class="content" />
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/Footer.vue'
import NavigationTop from '@/components/NavigationTop.vue'

export default {
  components: {
    Footer,
    NavigationTop,
  },
}
</script>

<style>
@import '@/assets/css/main.css';

.content {
  margin-top: 12vh;
}
</style>
