<template>
  <div>
    <div class="content splash">
      <div class="content ui container">
        <h1 class="page-title">ORIVESI ALLSTARS</h1>
        <h2 class="sub-title">The Great Happy Orchestra</h2>

        <SplashImages />
      </div>
    </div>

    <div class="content about">
      <img class="band-image" src="~/assets/images/oas-band.jpg" alt="">

      <div class="ui container">
        <h2>SUOMEN SUURIN PELIMANNIYHTYE</h2>
        <p>OAS eli Orivesi All Stars on kenelle tahansa soittamisen perustaidot omaavalle avoin pelimannikollektiivi, joka on perustettu musiikillisen ilon löytämisen, oppimisen, kokemisen ja jakamisen edistämiseksi. Ikähaitari OASissa on n.8-85 vuoden välillä, maantieteellinen kattavuus on jo vähintäänkin akselilla Saksa-Oulu-USA ja ryhmässä ei tehdä eroa, oletko amatööri-, harrastaja- vai ammattisoittaja. Ainoa päämäärä on, että harjoitetaan mukavaa ja mielekästä musisointia yhdessä, hyvässä hengessä ja annetaan sen näkyä ja kuulua!</p>
        <p>Yhtye on perustettu perinteisillä Oriveden kansanmusiikkikursseilla (järjestäjä Suomen Kansanmusiikkiliitto) joulukuussa vuonna 2011. Vetäjinä toimivat Antti Järvelä ja Reetta Kuisma.</p>
        <p><b>Tervetuloa mukaha!</b></p>
      </div>

    </div>
  </div>
</template>

<script>
import SplashImages from '@/components/SplashImages.vue'


export default {
  components: {
    SplashImages,
  }
}
</script>

<style scoped>
.sub-title {
  color: var(--accent-color);
}

.content {
  display:flex;
  flex-direction: column;
  justify-content: center;
}

.splash {
  height: 100vh;
  width: 100%;
}

.band-image {
  height: 670px;
  width: 100%;  
  object-fit: cover;
  object-position: top;
}
</style>