<template>
  <div>
    <table class="score-table">
      <tr class="header-row">
        <th>Nimi</th>
        <th>Säveltäjä</th>
        <th>Tanssilaji</th>
        <th>Versio</th>
        <th></th>
      </tr>
      <tr class="data-row">
        <td>For Sara</td>
        <td>Antti Järvelä</td>
        <td>Valssi</td>
        <td>
          <select name="versions" id="versions">
            <option value="volvo">Bb_Menuett-Jungfrun-träder-fram</option>
            <option value="saab">Saab</option>
            <option value="mercedes">Mercedes</option>
            <option value="audi">Audi</option>
          </select>
        </td>
        <td>
          <div id="data-icons">
            <i class="fas fa-download fa-lg"></i>
            <i class="fas fa-expand-alt fa-lg"></i>
          </div>
        </td>
      </tr>


      <tr class="data-row">
        <td>For Sara</td>
        <td>Antti Järvelä</td>
        <td>Valssi</td>
        <td>
          <select name="versions" id="versions">
            <option value="volvo">BMW</option>
            <option value="saab">Saab</option>
            <option value="mercedes">Mercedes</option>
            <option value="audi">Audi</option>
          </select>
        </td>
        <td>
          <div id="data-icons">
            <i class="fas fa-download fa-lg"></i>
            <i class="fas fa-expand-alt fa-lg"></i>
          </div>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  components: {
  },
}
</script>

<style scoped>
.score-table {
  width: 100%;
  text-align: left;
}

.header-row, .data-row {
  height: 75px;  
  background-color: #fafafa;
}

tr {
  text-align: center;
}

th, td {
  padding: 25px;
}

td {
  font-weight: 600;
}

select {
  width: 100%;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 5px;
  padding: 5px;
}

i {
  margin: 0 12px;
}

.data-row:hover {
  background-color: #f3f3f3;
  cursor: pointer;
}

#data-icons {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}
</style>