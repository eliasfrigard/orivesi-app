<template>
  <div class="main-wrapper" :style="{ backgroundColor: backgroundColor }">
    <div class="ui container wrapper">
      <h2 :style="{ color: textColor }">UUTISET</h2>
      <div class="previews">
        <NewsPreview class="preview" :textColor="textColor" image="oas6.jpg" />
        <NewsPreview class="preview" :textColor="textColor" image="OAS_levykuva.jpg" />
        <NewsPreview class="preview" :textColor="textColor" image="oas1.jpg" />
        <NewsPreview class="preview" :textColor="textColor" image="oas4.jpg" />
        <NewsPreview class="preview" :textColor="textColor" image="oas5.jpg" />
        <NewsPreview class="preview" :textColor="textColor" image="oas8.jpg" />
      </div>
    </div>
  </div>
</template>

<script>
import NewsPreview from '@/components/NewsPreview.vue'

export default {
  components: {
    NewsPreview,
  },
  props: {
    textColor: {
      type: String,
      default: 'black'
    },
    backgroundColor: {
      type: String,
      default: 'var(--accent-color)'
    }
  }
}
</script>

<style scoped>
.main-wrapper {
  color: rgb(240, 240, 240);
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
  padding-bottom: 15px;
}

.preview {
  margin-top: 60px;
}
</style>