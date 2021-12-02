<template>
  <div>
    <div class="score-container ui container">
      <MusicScores />
    </div>
  </div>
</template>

<script>
import MusicScores from '@/components/MusicScores.vue'

export default {
  components: {
    MusicScores,
  },
}
</script>

<style scoped>
.score-container {
  min-height: 100vh;
}

.score {
  width: 100%;
  height: 100vh;
  margin: 100px 0;
}
</style>
