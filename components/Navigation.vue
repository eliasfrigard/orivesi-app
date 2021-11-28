<template>
  <div class="nav">
    <NuxtLink class="navitem" to="/">Koti</NuxtLink>
    <NuxtLink class="navitem" to="/news">Uutiset</NuxtLink>
    <NuxtLink class="navitem" to="/events">Tapahtumat</NuxtLink>
    <NuxtLink class="navitem" to="/scores">Nuotit</NuxtLink>
    <NuxtLink class="navitem" to="/">Media</NuxtLink>
    <NuxtLink class="navitem" to="/">Jäsenyydet</NuxtLink>
    <NuxtLink class="navitem" to="/contact">Yhteistiedot</NuxtLink>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.nav {
  margin: 25px 0;
  width: 765px;
  display:flex;
  justify-content: space-between;
}

.navitem {
  color: black;
}

.navitem:hover {
  color: var(--accent-color);
}
</style>