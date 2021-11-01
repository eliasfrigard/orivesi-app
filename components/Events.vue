<template>
  <div class="ui container events">
    <div class="event-previews">
      <h2>TULEVAT TAPAHTUMAT</h2>
      <Event title="Ei Tulevia Tapahtumia" />

      <Event date="2020-08-05T14:00:43.511Z" location="Helsinki" country="FI" title="Jamit Pasilan kirjastossa" />
      <Event date="2019-02-17T14:00:43.511Z" location="Helsinki" country="FI" title="OAS ry:n vuosikokous" />
      <Event date="2020-07-02T16:00:43.511Z" location="Helsinki" country="FI" title="Kurssi Oulussa Kurssi Espoossa (tarkentuu)" />
      <Event date="2022-05-13T18:00:43.511Z" location="Helsinki" country="FI" title="Perinteiset Oriveden kurssit (järj. Suomen Kansanmusiikkiliitto)"/>
      <Event date="2020-08-05T14:00:43.511Z" location="Helsinki" country="FI" title="Jamit Pasilan kirjastossa" />
      <Event date="2019-02-17T14:00:43.511Z" location="Helsinki" country="FI" title="OAS ry:n vuosikokous" />
      <Event date="2020-07-02T16:00:43.511Z" location="Helsinki" country="FI" title="Kurssi Oulussa Kurssi Espoossa (tarkentuu)" />
      <Event date="2022-05-13T18:00:43.511Z" location="Helsinki" country="FI" title="Perinteiset Oriveden kurssit (järj. Suomen Kansanmusiikkiliitto)"/>
    </div>

    <div v-if="!onlyUpcoming" class="event-previews">
      <h2 class="old-events-title">VANHAT TAPAHTUMAT</h2>  
      <Event date="2020-08-05T14:00:43.511Z" location="Helsinki" country="FI" title="Jamit Pasilan kirjastossa" />
      <Event date="2019-02-17T14:00:43.511Z" location="Helsinki" country="FI" title="OAS ry:n vuosikokous" />
      <Event date="2020-07-02T16:00:43.511Z" location="Helsinki" country="FI" title="Kurssi Oulussa Kurssi Espoossa (tarkentuu)" />
      <Event date="2022-05-13T18:00:43.511Z" location="Helsinki" country="FI" title="Perinteiset Oriveden kurssit (järj. Suomen Kansanmusiikkiliitto)"/>
      <Event date="2020-08-05T14:00:43.511Z" location="Helsinki" country="FI" title="Jamit Pasilan kirjastossa" />
      <Event date="2019-02-17T14:00:43.511Z" location="Helsinki" country="FI" title="OAS ry:n vuosikokous" />
      <Event date="2020-07-02T16:00:43.511Z" location="Helsinki" country="FI" title="Kurssi Oulussa Kurssi Espoossa (tarkentuu)" />
      <Event date="2022-05-13T18:00:43.511Z" location="Helsinki" country="FI" title="Perinteiset Oriveden kurssit (järj. Suomen Kansanmusiikkiliitto)"/>
      <Event date="2020-08-05T14:00:43.511Z" location="Helsinki" country="FI" title="Jamit Pasilan kirjastossa" />
    </div>
  </div>
</template>

<script>
import Event from '@/components/Event.vue'

export default {
  components: {
    Event
  },
  props: {
    onlyUpcoming: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
.event-previews {
  display:flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.events {
  display:flex;
  flex-direction: column;
  align-items: center;
}

h2 {
  margin-bottom: 45px;
}

.old-events-title {
  margin-top: 100px;
}
</style>