<template>
  <div class="ui container events">
    <Events />
  </div>
</template>

<script>
import Events from '@/components/Events.vue'

export default {
  components: {
    Events,
  },
}
</script>

<style scoped>
.news {
  min-height: 100vh;
}

.events {
  margin: 100px 0;
}
</style>