<template>
    <div class="containerChild">
        <h3></h3>
    </div>
</template>

<script steup lang="ts">
import type { IAlumnos } from '@/interfaces/IAlumnos';
import { ref } from 'vue'

const props = defineProps<IAlumnos>()

console.log(props.ApellidoMaternoAlumno)

</script>

<style scoped>
.containerChild{
    display: flex;
    justify-content: center;
    padding: 1.5rem;
    border: 0.25rem solid #3bc769;
    border-radius: 0.75rem; 
    background-color: #92D1B3;
}
</style>