<template>
  <div class="score">
    <p class="title">2-Rivisjenkka</p>
  </div>
</template>

<script>
export default {
  name: 'MusicScore'  
}
</script>

<style scoped>
.score {
  width: 100%;
  min-height: 150px;
  background-color: #fafafa;
  border: 1px solid rgba(14, 19, 57, 0.2);
  border-radius: 5px;
  padding: 20px;
}

.title {
  font-weight: 600;
  transition: all 100ms ease-in-out;
}
</style>