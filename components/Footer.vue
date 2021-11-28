<template>
  <div class="footer accent-background">
    <div class="footer-content ui container">
      <div class="footer-div">
        <NuxtLink class="navitem" to="/">Koti</NuxtLink>
        <NuxtLink class="navitem" to="/news">Uutiset</NuxtLink>
        <NuxtLink class="navitem" to="/events">Tapahtumat</NuxtLink>
        <NuxtLink class="navitem" to="/">Nuotit</NuxtLink>
        <NuxtLink class="navitem" to="/">Media</NuxtLink>
        <NuxtLink class="navitem" to="/">Jäsenyydet</NuxtLink>
        <NuxtLink class="navitem" to="/contact">Yhteistiedot</NuxtLink>
      </div>
      <div class="footer-div">
        <p>Media</p>
      </div>
      <div class="footer-div">
        <p>Made by Elias Frigård</p>
        <a href="mailto:elias@orivesiallstars.fi">elias@orivesiallstars.fi</a>
        <br>
        <p>Copyright © Orivesi All Stars 2021</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.footer {
  color: white;
  height: 350px;
  background-color: var(--accent-color);

  display:flex;
}

.footer-content {
  padding: 50px 0;
  display:flex;
  justify-content: space-evenly;
}

.footer-div {
  display: flex;
  flex-direction: column;
}

a {
  color: white;
  font-size: 16px;
  font-weight: 600;
}

p {
  font-size: 16px;
}
</style>