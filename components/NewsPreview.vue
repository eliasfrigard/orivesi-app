<template>
  <div class="news-preview">
    <div class="image-wrapper">
      <img class="image" :src="'./images/' + image" alt="" />
    </div>

    <div class="text" :style="{ color: textColor }">
      <a :style="{ color: textColor }">
        ”Kaikenmoisia tansseja” on valittu vuoden kansanmusiikkilevyksi!!
      </a>
      <p class="meta">Kategoria / Päivämäärä</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    textColor: {
      type: String,
      default: 'black',
    },
    image: String,
    title: String,
  },
}
</script>

<style scoped>
.news-preview {
  -webkit-box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.1),
    5px 5px 5px 1px rgba(0, 0, 0, 0);
  box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.1),
    5px 5px 5px 1px rgba(0, 0, 0, 0);
  cursor: pointer;
  width: calc(33.33% - 25px);
  outline: 5px solid rgba(255, 255, 255, 0.15);
  outline-offset: 0.5em;
}

.image-wrapper {
  /*   border-radius: 10px 10px 0 0;
 */
  overflow: hidden;
}

.image {
  width: 100%;
  height: 250px;
  object-fit: cover;
  transition: all 100ms ease-in-out;
}

.text {
  background-color: rgba(255, 255, 255, 0.15);
  padding: 20px;
  /*   border-radius: 0 0 10px 10px;
 */
  word-wrap: break-word;
}

a {
  letter-spacing: 1.5px;
  text-decoration: none;
  font-family: 'Athiti', sans-serif;
  font-size: 19px;
  font-weight: 600;

  background-image: linear-gradient(
    90deg,
    rgba(218, 85, 78, 0),
    rgba(218, 85, 78, 0)
  );
  background-repeat: no-repeat;
  background-position: bottom left;
  background-size: 0% 2px;
  transition: background-size 400ms ease-in-out;
}

.news-preview:hover {
  /*   -webkit-box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.2),
    5px 5px 5px 1px rgba(0, 0, 0, 0);
  box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.2),
    5px 5px 5px 1px rgba(0, 0, 0, 0); */
  outline: 7px solid rgba(255, 255, 255, 0.2);
}

.news-preview:hover a {
  color: white;
  background-size: 100% 2px;
}

.news-preview:hover .image {
  transform: scale(1.05);
}

.meta {
  font-size: 16px;
  margin-top: 10px;
  letter-spacing: 1.5px;
}
</style>
