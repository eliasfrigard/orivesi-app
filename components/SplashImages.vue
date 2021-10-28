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
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.images {
  margin-top: 20px;
  display:flex;
  flex-wrap: wrap;
  width: 75%;
}
.image {
  height: 150px;
  width: 150px;  
  object-fit: cover;
  margin: 10px 10px 0 0 ;
}
</style>