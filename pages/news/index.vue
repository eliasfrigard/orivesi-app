<template>
  <div class="ui container news">
    <NewsPreviews backgroundColor="white" textColor="black" class="previews" />
  </div>
</template>

<script>
import NewsPreviews from '@/components/NewsPreviews.vue'

export default {
  components: {
    NewsPreviews,
  },
}
</script>

<style scoped>
.news {
  min-height: 100vh;
}

.previews {
  margin: 100px 0;
}
</style>