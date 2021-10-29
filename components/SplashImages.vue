<template>
  <div class="images">
    <img class="image" src="~/assets/images/oas1.jpg" alt="">
    <img class="image" src="~/assets/images/oas2.jpg" alt="">
    <img class="image" src="~/assets/images/oas3.jpg" alt="">
    <img class="image" src="~/assets/images/oas4.jpg" alt="">
    <img class="image" src="~/assets/images/oas5.jpg" alt="">
    <img class="image" src="~/assets/images/oas6.jpg" alt="">
    <img class="image" src="~/assets/images/oas7.jpg" alt="">
    <img class="image" src="~/assets/images/oas8.jpg" alt="">
    <img class="image" src="~/assets/images/oas9.jpg" alt="">
    <img class="image" src="~/assets/images/oas10.jpg" alt="">
    <img class="image" src="~/assets/images/oas11.jpg" alt="">
    <img class="image" src="~/assets/images/oas12.jpg" alt="">
    <img class="image" src="~/assets/images/oas13.jpg" alt="">
    <img class="image" src="~/assets/images/oas14.jpg" alt="">
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.images {
  margin-top: 20px;
  display:flex;
  flex-wrap: wrap;
  width: 100%;
}
.image {
  width: calc(14.285% - 10px);
  margin: 10px 10px 0 0;
  object-fit: cover;
}
</style>