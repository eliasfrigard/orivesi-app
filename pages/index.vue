<template>
  <div>
    <div class="content splash">
      <div class="content ui container">
        <h1 class="page-title">ORIVESI ALL STARS</h1>
        <h2 class="sub-title">the great happy orchestra</h2>
        <Navigation />
        <SplashImages />
      </div>
    </div>

    <div class="content about">
      <img class="band-image" src="~/assets/images/oas-band.jpg" alt="" />

      <div class="ui container info-wrapper">
        <div class="info-container">
          <div v-html="infoText"></div>
        </div>
      </div>

      <div class="wavy-container">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
          <path
            fill="#D57B01"
            fill-opacity="1"
            d="M0,64L120,58.7C240,53,480,43,720,37.3C960,32,1200,32,1320,32L1440,32L1440,320L1320,320C1200,320,960,320,720,320C480,320,240,320,120,320L0,320Z"
          ></path>
        </svg>

        <h2>TULEVAT TAPAHTUMAT</h2>

        <!--         <NewsPreviews class="news" textColor="white" />
 -->
        <div class="flip">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
            <path
              fill="#FFF"
              fill-opacity="1"
              d="M0,192L120,181.3C240,171,480,149,720,149.3C960,149,1200,171,1320,181.3L1440,192L1440,320L1320,320C1200,320,960,320,720,320C480,320,240,320,120,320L0,320Z"
            ></path>
          </svg>
        </div>
      </div>

      <Events onlyUpcoming="true" />

      <div class="album">
        <div class="text-divider">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
            <path
              fill="#D57B01"
              fill-opacity="1"
              d="M0,96L1440,0L1440,320L0,320Z"
            ></path>
          </svg>
          <div class="album-title accent-background">
            <h2>KAIKENMOISIA TANSSEJA</h2>
            <br />
            <h3>VUODEN KANSANMUSIIKKIVELY 2020</h3>
          </div>

          <div class="flip">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
              <path
                fill="#D57B01"
                fill-opacity="1"
                d="M0,96L1440,0L1440,320L0,320Z"
              ></path>
            </svg>
          </div>
        </div>

        <div class="ui container album-content">
          <img
            class="album-image"
            src="~/assets/images/OAS_levykuva.jpg"
            alt=""
          />
          <div class="info-container">
            <div v-html="albumText"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import DOMPurify from 'dompurify'
import { marked } from 'marked'

import SplashImages from '@/components/SplashImages.vue'
/* import NewsPreviews from '@/components/NewsPreviews.vue'
 */ import Events from '@/components/Events.vue'
import Navigation from '@/components/Navigation.vue'

export default {
  components: {
    SplashImages,
    /*     NewsPreviews,
     */ Events,
    Navigation,
  },
  data() {
    return {
      title: '',
      subtitle: '',
      infoText: '',
    }
  },
  created() {
    /* Get single page data. */
    axios.get('https://orivesiallstars.net/home').then((response) => {
      const data = response.data

      this.infoText = DOMPurify.sanitize(marked(data.InfoText))
      this.albumText = DOMPurify.sanitize(marked(data.AlbumText))
    })
  },
}
</script>

<style scoped>
.sub-title {
  color: var(--accent-color);
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.splash {
  height: 100vh;
  width: 100%;
}

.band-image {
  max-height: 900px;
  width: 100%;
  object-fit: cover;
  object-position: top;
  -webkit-box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.3),
    5px 5px 5px 1px rgba(0, 0, 0, 0);
  box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.3),
    5px 5px 5px 1px rgba(0, 0, 0, 0);
}

.info-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}

.info-container {
  margin: 100px 0;
  max-width: 965px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  text-align: center;
}

.ininfo-containerfo h2,
.info-container p {
  margin: 15px;
}

.button {
  width: 150px;
  height: 50px;
  margin: 25px;
  background-color: var(--accent-color);
  outline: 4px solid var(--accent-color);
  outline-offset: 0.25em;
  color: white;
  font-size: 16px;
}

.button:hover {
  background-color: var(--accent-hover);
  outline: 4px solid white;
}

.wavy-container .flip {
  background-color: var(--accent-color);
  transform: translateY(-150px);
  margin-bottom: -150px;
}

.flip {
  transform: rotate(180deg);
}

.album {
  margin-bottom: 50px;
}

.album-title {
  background-color: var(--accent-color);
  color: white;
  text-align: center;
  outline: 5px solid var(--accent-color);

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.album-content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.album-content .info-container {
  max-width: 100%;
  margin: 100px 0;
}

.album-image-wrapper {
  width: 100%;
  background-image: url('~/assets/images/album-background.svg');
  background-repeat: no-repeat;
}

.semi-bold {
  font-weight: 600;
}

.text-divider {
  margin: 150px 0;
}

.news {
  transform: translateY(-150px);
}
</style>
