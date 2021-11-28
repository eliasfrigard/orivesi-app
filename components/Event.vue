<template>
  <div class="event">
    <div class="highlight"></div>
    <div class="content">
      <div class="date">
        <p class="day">{{day}}</p>
        <p class="month">{{month}}</p>
        <p class="year">{{year}}</p>
      </div>

      <div class="text">
        <p class="title">{{ title }}</p>
      </div>
        <p class="location">{{ location }}, {{ country }} <i :class="flagClass"></i></p>
    </div>
  </div>
</template>

<script>
import moment from 'moment'

export default {
  props: {
    title: String,
    date: {
      type: String,
      default: ''
    },
    location: String,
    country: String
  },
  computed: {
    flagClass() {
      if (this.date === '') {
        return ''
      }

      return /* this.country.toLowerCase() */ 'fi' + ' flag'
    },
    day() {
      if (this.date === '') {
        return ''
      }

      return moment(this.date).format('DD')
    },
    month() {
      if (this.date === '') {
        return ''
      }

      let month = ""
      const engMonth = moment(this.date).format('MMMM')

      switch (engMonth) {
        case "January":
          month = "Tammi"
          break;
        case "February":
          month = "Helmi"
          break;
        case "March":
          month = "Maalis"
          break;
        case "April":
          month = "Huhti"
          break;
        case "May":
          month = "Touko"
          break;
        case "June":
          month = "Kesä"
          break;
        case "July":
          month = "Heinä"
          break;
        case "August":
          month = "Elo"
          break;
        case "September":
          month = "Syys"
          break;
        case "October":
          month = "Loka"
          break;
        case "November":
          month = "Marras"
          break;
        case "December":
          month = "Joulu"
          break;
      }

      return month
    },
    year() {
      if (this.date === '') {
        return ''
      }

      return moment(this.date).format('YYYY')
    }
  },
}
</script>

<style scoped>
.event {
  margin:15px 0;

  width: 100%;
  height: 120px;
  background-color: #fafafa;
  border: 1px solid rgba(14, 19, 57, 0.2);
  border-radius: 5px;
  cursor: pointer;

  display: flex;

  transition: all 100ms ease-in-out;
}

.content {
  height: 100%;
  width: calc(100% - 7px);
  display:flex;
  justify-content: space-between;
  align-items: center;
}

.highlight {
  height:100%;
  width: 3px;

  border-radius: 5px 0 0 5px;
  background-color: var(--accent-color);
  transition: all 100ms ease-in-out;
}

.event:hover .highlight {
  width: 8px;
  margin-right: -5px;
}


.event:hover {
  background-color: #f3f3f3;
}

.date {
  width: 125px;
  margin:15px;
  display: flex;
  flex-direction: column;
}

.day, .month, .year {
  margin: 0;
  padding: 0;
  line-height: 100%;
}

.day {
  text-align: center;
  line-height: 85%;
  margin:0;
  font-size:50px;
  font-weight: 600;
}

.month {
  margin: 0;
  text-align: center;
  font-size: 24px;
  line-height: 110%;
}

.year {
  margin: 0;
  text-align: center;
  font-size: 18px;
}

.title, .location {
  text-transform: uppercase;
}

.title {
  font-weight: 600;
  text-align: center;
  transition: all 100ms ease-in-out;
}

.location {
  margin:15px;
  min-width: 125px;
}

.text {
  margin: 15px;
  display:flex;
  flex-direction: column;
}
</style>