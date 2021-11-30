<template>
  <div>
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/Footer.vue'
import Header from '@/components/Header.vue'

export default {
  components: {
    Footer,
    Header,
  },
}
</script>

<style>
.header {
  top: 100vh;
}

:root {
  --accent-color: #d57b01;
  --accent-hover: #eca202;
}

::selection {
  color: white;
  background: #d57b01; /* WebKit/Blink Browsers */
}

::-moz-selection {
  color: white;
  background: #d57b01; /* Gecko Browsers */
}

.accent-background ::selection {
  color: #d57b01;
  background: white; /* WebKit/Blink Browsers */
}

html {
  font-family: 'Antonio', sans-serif;
  letter-spacing: 0.5px;
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

p,
th,
td {
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
  color: var(--accent-hover);
}
</style>
