<template>
  <div class="container">
    <div class="title">
      <h1>Actividad 3</h1>
      <h2>Lista de Datos</h2>
    </div>
    
    <div class="content">
      <button @click="direccionarSinRouter" v-if="!rutaActual"> Chan Garduño Eduardo </button>
      <div class="listado" v-else>
          <cAlumnos v-bind="CalificacionesData[0]" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import CalificacionesData from '@/data/AlumnosData'
import { ref } from 'vue'
import cAlumnos from '@/components/cAlumnos.vue'

const rutaActual = ref(false)

function direccionarSinRouter() {
  rutaActual.value = !rutaActual.value
}

</script>

<style scoped>
/* .container{
  background-color: red;
} */
 h1{
  font-weight: bolder;
 }
  h2{
    font-weight: bold;
  }
.title{
  text-align: center;
  padding: 2rem;
  margin-bottom: 1rem;
  border: 0.25rem solid #3bc769;
  border-radius: 0.75rem;
  background-color: #89C893;
  color: #fff;
}
.content{
  display: flex;
  justify-content: center;
  padding: 1.5rem;
  border: 0.25rem solid #3bc769;
  border-radius: 0.75rem; 
  background-color: #89C893;
}
button{
  padding: 0.5rem;
  border-radius: 0.75rem;
  font-size: 1rem;
  color: #fff;
  background-color: #49896F;
  cursor: pointer;
}
</style>