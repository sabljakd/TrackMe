<template>
<div id="tezina">
  <div class="graf">
      <h1>Tezina</h1>
    <ve-line :data="chartData"></ve-line>
  </div>
<div class="row">
  <div class="col-sm-5" >
    <div class="card-header">
    Tezina
  </div>
  <ul class="list-group list-group-flush">
    <li class="list-group-item">99.5</li>
    <li class="list-group-item">99.2</li>
    <li class="list-group-item">99</li>
  </ul>
  </div>
  <div class="col-sm-5">
    <div class="card-header">
    Datum unosa
  </div>
  <ul class="list-group list-group-flush">
    <li class="list-group-item">20.01.2020</li>
    <li class="list-group-item">23.01.2020</li>
    <li class="list-group-item">26.01.2020</li>
  </ul>
  </div>
</div>

</div>

</template>

<script>
import VeLine from 'v-charts/lib/line.common'
export default {
  components: { VeLine },
  data () {
    return {
      chartData: {
        columns: ['datum', 'Kilaza u Kg'],
        rows: [
          { 'datum': '10-02', 'Kilaza u Kg': 100 },
          { 'datum': '15-02', 'Kilaza u Kg': 99.6 },
          { 'datum': '01-03', 'Kilaza u Kg': 99.5 },
          { 'datum': '01-04', 'Kilaza u Kg': 99.5 },
          { 'datum': '01-05', 'Kilaza u Kg': 99.4 },
          { 'datum': '01-06', 'Kilaza u Kg': 99.2 },
          { 'datum': '01-07', 'Kilaza u Kg': 99 },
          { 'datum': '01-08', 'Kilaza u Kg': 98.5 },
          { 'datum': '01-09', 'Kilaza u Kg': 98.4 },
          { 'datum': '01-10', 'Kilaza u Kg': 98.2 },
          { 'datum': '01-11', 'Kilaza u Kg': 97 },
          { 'datum': '01-12', 'Kilaza u Kg': 97 },
          { 'datum': '01-13', 'Kilaza u Kg': 97.3 },
          { 'datum': '01-14', 'Kilaza u Kg': 97.2 },
          { 'datum': '01-15', 'Kilaza u Kg': 96 }
        ]
      }
    }
  }
}
</script>
<style scoped>

.graf {
  margin-top: 100px;
  margin-bottom: 100px;
  margin-right: 300px;
  margin-left: 400px;
}

.row{
    margin-left:350px;
}





</style>