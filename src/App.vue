<template>

  <div class="container mt-4">
    <h1 class="text-center text-primary" >Bienvenido CLA a la programación con {{ titulo }} </h1>

    <h3 class="text-secondary" >Probando VUE</h3>

    <h3 v-bind:class="textWarning" >Probando VUE con v-bind</h3>

    <h3 :class="textInfo" >Probando VUE con : (v-bind simplificado) </h3>

    <!-- Uso del operador ternario --->

    <h3> {{ estado ? 'El estado es verdadero (operador ternario)' : 'El estado es falso (operador ternario)' }} </h3>

    <!-- v-if - v-else-if - v-else --->

    <h3 v-if="estadoVif">El estado es verdadero (v-if / v-else) </h3>
    <h3 v-else>El estado es falso (v-if / v-else) </h3>

    <h3 class='text-danger' v-if="estadoVifElseif === true" >El estado es verdadero (v-if / v-else-if) </h3>
    <h3 class='text-danger' v-else-if ="estadoVifElseif === false"  >El estado es falso (v-if / v-else-if) </h3>
    <h3 class='text-danger' v-else>El estado es otro (v-if / v-else-if) </h3>

    <h3 class='text-primary' > {{ paises }} </h3>

    <div class="col-3">
      <ul class="list-group ">
        <li class="list-group-item  text-success" v-for="(pais,index) in paises" :key="index"> {{ index }} - {{ pais }} </li>
      </ul>
    </div>

    <div class="col-4">
      <ul class="list-group ">
        <li class="list-group-item  text-success" v-for="(item,index) in paisesCompletos" :key="index"> {{ item.nombre }} - {{ item.capital }} - {{ item.poblacion }} </li>
      </ul>
    </div>

    <br>
    <br>



  </div>








</template>

<script setup>

  const titulo = 'VUEjs 3.0.0';
  const textWarning = 'text-warning';
  const textInfo = 'text-info';
  const estado = false;

  const estadoVif = true;

  const estadoVifElseif = null;

  const paises = ['Argentina', 'Brasil', 'Uruguay', 'Chile', 'Colombia'];

  const paisesCompletos = [

    { nombre: 'Argentina', 
      capital: 'Buenos Aires', 
      poblacion: 4500, 
    },

    { nombre: 'Brasil', 
      capital: 'Brasilia',
      poblacion: 12000, 
    },

    { nombre: 'Uruguay', 
      capital: 'Montevideo',
      poblacion: 400, 
    },

    { nombre: 'Chile', 
      capital: 'Santiago',
      poblacion: 1000, 
    },

    { nombre: 'Colombia', 
      capital: 'Bogotá',
      poblacion: 3000, 
    },
  ]



</script>

<style>

</style>
