<template>
  <div class="ui container events">
    <h2>TULEVAT TAPAHTUMAT</h2>
    <Event date="2020-08-05T14:00:43.511Z" title="Jamit Pasilan kirjastossa" />
    <Event date="2019-02-17T14:00:43.511Z" title="OAS ry:n vuosikokous" />
    <Event date="2020-07-02T16:00:43.511Z" title="Kurssi Oulussa Kurssi Espoossa (tarkentuu)" />
    <Event date="2022-05-13T18:00:43.511Z" title="Perinteiset Oriveden kurssit (järj. Suomen Kansanmusiikkiliitto)"/>
  </div>
</template>

<script>
import Event from '@/components/Event.vue'

export default {
  components: {
    Event
  }
}
</script>

<style scoped>
.events {
  display:flex;
  flex-direction: column;
  align-items: center;
}

h2 {
  margin-bottom: 45px;
}
</style>