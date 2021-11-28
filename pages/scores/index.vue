<template>
  <div>
    <div class="score-container ui container">
      <iframe class="score" src="/2-rivisJenkka.pdf"></iframe>
    </div>
  </div>
</template>

<script>
export default {
  components: {
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