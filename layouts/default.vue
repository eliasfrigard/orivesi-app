<template>
  <div>
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/Footer.vue'

export default {
  components: {
    Footer
  }
}
</script>

<style>
:root {
  --accent-color: #D57B01;
  --accent-hover: #eca202;
}

::selection {
  color: white;
  background: #D57B01; /* WebKit/Blink Browsers */
}
::-moz-selection {
  color: white;
  background: #D57B01; /* Gecko Browsers */
}

html {
  font-family: 'Antonio', sans-serif;
  letter-spacing: .5px;
}

h1 {
  font-size: 84px;
  font-weight: bold;
  letter-spacing: 1px;
}

h2 {
  font-size: 55px;
  font-weight: bold;
  letter-spacing: 1px;
}

h3 {
  font-size: 24px;
  letter-spacing: 1px;
}

p {
  font-family: 'Athiti', sans-serif;
  font-size: 20px;
  line-height: 35px;
}

a {
  font-family: 'Athiti', sans-serif;
  font-size: 20px;
  text-transform: uppercase;
  font-weight: 600;
  letter-spacing: 1px;
  color: var(--accent-color);
  line-height: 35px;
}

a:hover {
  color: var(--accent-hover)
}
</style>