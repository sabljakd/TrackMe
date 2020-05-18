<template>
<div id="container">
<div class="row">
  <div class="col-sm-6">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Dodaj kalorije</h5>
        <p class="card-text">Upisite sto ste jeli da bi pratili unos kalorija</p>

        <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Naziv" aria-label="Naziv" aria-describedby="basic-addon1">
            <input type="text" class="form-control" placeholder="Datum" aria-label="Date" aria-describedby="basic-addon1">
        </div>
        <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Kalorija po 100 g/ml" aria-label="kalorijapo" aria-describedby="basic-addon1">
            <input type="text" class="form-control" placeholder="Kolicina (g/ml)" aria-label="kolicinapo" aria-describedby="basic-addon1">
        </div>
        

        <button @click="Alert" class="btn btn-dark">Dodaj</button>  
        
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Dodaj tezinu</h5>
        <p class="card-text">Upisujte svoju tezinu da bi dobivali tocne informacije</p>

        <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Tezina (Kg)" aria-label="tezina" aria-describedby="basic-addon1">
        </div>
        <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Datum" aria-label="date" aria-describedby="basic-addon1">
        </div>
        

        <button @click="Alert" class="btn btn-dark">Dodaj</button> 
      </div>
    </div>
  </div>
</div>

<div id="app">
    <div class="container-fluid">
        <div class="row">
            <div class=" col-md-12">
                <h1>Moja visina :{{ height }} cm</h1>
                <input v-model="height">
                <h1>Moja tezina :{{ weight }} kg</h1>
                <input v-model="weight">
              
                <h2>My BMI is (moram fixati js kod) {{ bmi }}</h2>
            </div>
        </div>
    </div>
</div>
</div>


</template>

<script>
import Swal from 'sweetalert2'

export default {
    name: 'bmi',
    data(){
      return{
        height: null ,
        weight: null,
      }
    },
   
   
    methods: { 
        
           
    bmi: function() {
      var weight = parseInt(this.weight);
      var height = parseInt(this.height) / 100;
      var bmi = weight / (height * height)
      if(bmi < 25) {
        return 'Low: ' + bmi.toFixed(2) + 'kg/m2';
      }
      else if (bmi >=25 && bmi <30 ) {
        return 'Moderate: ' + bmi.toFixed(2) + 'kg/m2';
      }
      else if (bmi >=30 ) {
        return 'High: ' + bmi.toFixed(2) + 'kg/m2';
      }
    },
    Alert() {
      // Use sweetalert2
      Swal.fire({
  title: 'Uspjesno spremljeno!',
  text: 'Hvala na koristenju aplikacije.',
  
})
    },
    }

}

  
 

</script>
<style scoped>

#container {
    margin-top: 150px;
    margin-left: 200px;
    margin-right: 20px;
}

.btn{
    margin-left: 10px;
}

#app {
    
    border: solid black;
    padding: 1px;
    margin-top: 10px;
}


</style>