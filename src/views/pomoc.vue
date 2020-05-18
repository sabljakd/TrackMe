<template>
    <form>
  <div class="form-group">
    <label for="exampleFormControlInput1">Tvoja Email Adresa</label>
    <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="mail@primjer.com">
  </div>
  

  <div class="form-group">
    <label for="exampleFormControlTextarea1">Poruka za nas</label>
    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
  </div>
  <button @click="Alert" class="btn btn-dark">Posalji</button>
</form>

</template>

<script>
import Swal from 'sweetalert2'

export default {
    methods: { 
        
    Alert() {
      // Use sweetalert2
      Swal.fire({
  title: 'Uspjesno poslano!',
  
})
    },
    }

}

  
 

</script>

<style scoped>

form {
    margin-top:50px;
    margin-right: 200px;
    margin-left:360px;

}

</style>