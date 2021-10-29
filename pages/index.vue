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

      <div class="ui container info-wrapper">
        <div class="info">
          <h2>Suomen Suurin Pelimanniyhtye</h2>
          <p>OAS eli Orivesi All Stars on kenelle tahansa soittamisen perustaidot omaavalle avoin pelimannikollektiivi, joka on perustettu musiikillisen ilon löytämisen, oppimisen, kokemisen ja jakamisen edistämiseksi. Ikähaitari OASissa on n.8-85 vuoden välillä, maantieteellinen kattavuus on jo vähintäänkin akselilla Saksa-Oulu-USA ja ryhmässä ei tehdä eroa, oletko amatööri-, harrastaja- vai ammattisoittaja. Ainoa päämäärä on, että harjoitetaan mukavaa ja mielekästä musisointia yhdessä, hyvässä hengessä ja annetaan sen näkyä ja kuulua!</p>
          <p>Yhtye on perustettu perinteisillä Oriveden kansanmusiikkikursseilla (järjestäjä Suomen Kansanmusiikkiliitto) joulukuussa vuonna 2011. Vetäjinä toimivat Antti Järvelä ja Reetta Kuisma.</p>
          <p><b>Tervetuloa mukaha!</b></p>
        </div>
      </div>

      <div class="wavy-container">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#D57B01" fill-opacity="1" d="M0,64L120,58.7C240,53,480,43,720,37.3C960,32,1200,32,1320,32L1440,32L1440,320L1320,320C1200,320,960,320,720,320C480,320,240,320,120,320L0,320Z"></path></svg>        <NewsPreviews />
        <div class="flip">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#FFF" fill-opacity="1" d="M0,192L120,181.3C240,171,480,149,720,149.3C960,149,1200,171,1320,181.3L1440,192L1440,320L1320,320C1200,320,960,320,720,320C480,320,240,320,120,320L0,320Z"></path></svg>        
        </div>
      </div>

      <div class="events">
        <Concert date="2022-08-13T18:00:43.511Z" location="Helsinki" country="FI" link="http://" description="Jamit Pasilan Kirjastossa" />        
      </div>

      <div class="ui container">
        <img src="~/assets/images/OAS_levykuva.jpg" alt="">
      </div>

    </div>
  </div>
</template>

<script>
import SplashImages from '@/components/SplashImages.vue'
import NewsPreviews from '@/components/NewsPreviews.vue'
import Concert from '@/components/Concert.vue'


export default {
  components: {
    SplashImages,
    NewsPreviews,
    Concert
  }
}
</script>

<style scoped>
.sub-title {
  color: var(--accent-color);
/*   text-shadow: 
  0.025em 0.025em 0 yellow,
  0.05em 0.05em 0 blue,
  0.075em 0.075em 0 red; */
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
  max-height: 900px;
  width: 100%;  
  object-fit: cover;
  object-position: top;
  -webkit-box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.3), 5px 5px 5px 1px rgba(0,0,0,0); 
  box-shadow: 0px 10px 13px -7px rgba(0, 0, 0, 0.3), 5px 5px 5px 1px rgba(0,0,0,0);   
}

.info-wrapper {
  display:flex;
  justify-content: center;
  align-items: center;
}

.info {
  margin: 100px 0;
  max-width: 965px;
  display:flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  text-align: center;
}

.info h2, .info p {
  margin: 15px;
}

.button {
  width: 150px;
  height: 50px;
  margin:25px;
  background-color: var(--accent-color);
  outline: 4px solid var(--accent-color);
  outline-offset: .25em;
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
}

</style>