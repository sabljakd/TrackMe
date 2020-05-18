<template>
<div id="tezina">
  <div class="graf">
      <h1>Dnevnik unosa kalorija</h1>
    <ve-line :data="chartData"></ve-line>
  </div>
<div class="row">
  <div class="col-sm-5" >
    <div class="card-header">
    Unesene kalorije
  </div>
  <ul class="list-group list-group-flush">
    <li class="list-group-item" style="color:green">1498 cal</li>
    <li class="list-group-item" style="color:red">1501 cal</li>
    <li class="list-group-item" style="color:red">1550 cal</li>
    <li class="list-group-item" style="color:blue">900 cal</li>
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
    <li class="list-group-item">30.01.2020</li>
  </ul>
  </div>
</div>
<div>
  <p style="color:green">Unijeli ste dovoljno kalorija</p>
  <p style="color:red">Unijeli ste previse kalorija</p>
  <p style="color:blue">Niste unijeli dovoljno kalorija</p>
</div>

</div>

</template>

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

p {
  text-align: left;
  
  margin-left: 360px;
}





</style>