<template>
  <div class="nmPanel">
    <table>
      <thead>
        <tr>
          <td>Identificacion</td>
          <td>Empleado</td>
          <td>Salario</td>
          <td>HRN</td>
          <td>HED</td>
          <td>HEN</td>
          <td>HDF</td>
        </tr>
      </thead>
      <tr>
        <td>Identificacion</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
    </table>
  </div>
</template>

<script>
 export default {
   data() {
     return {
       items:[]
     }
   },
   created(){
     this.FectchItems();
   },
   methods: {
     FectchItems(){
       this.axios.Get('/items')
       .then(res => console.log(res))
       .catch(err => console.log(err));
     }
   }
 }
</script>
