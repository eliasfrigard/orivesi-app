<template>
  <div class="main-wrapper">
    <div class="ui container wrapper">
      <h2>UUTISET</h2>
      <div class="previews">
        <NewsPreview class="preview" image="OAS_levykuva.jpg" />
        <NewsPreview class="preview" image="oas1.jpg" />
        <NewsPreview class="preview" image="oas4.jpg" />
        <NewsPreview class="preview" image="oas5.jpg" />
        <NewsPreview class="preview" image="oas6.jpg" />
        <NewsPreview class="preview" image="oas8.jpg" />
      </div>
    </div>
  </div>
</template>

<script>
import NewsPreview from '@/components/NewsPreview.vue'

export default {
  components: {
    NewsPreview,
  }
}
</script>

<style scoped>
.main-wrapper {
  color: rgb(240, 240, 240);
  background-color: #D57B01;
  transform: translateY(-150px);
}

.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.previews {
  display:flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.preview {
  margin-top: 60px;
}
</style>