<template>
    <div class="country">
        <h1>Pais {{paisInfo}}</h1>

    </div>
</template>

<script setup>
import {onMounted, ref, watch } from 'vue';
import {useRoute} from 'vue-router';

const route = useRoute();
const paisInfo = ref();

watch(() => route.params.pais, newValue => {
    console.log('pais cambiado', newValue)
    paisInfo.value = findPais(route.params.pais)
})

onMounted(() =>{
    console.log('componente montado')
    paisInfo.value = findPais(route.params.pais)
})

//simular la bussqueda del pais
const findPais = (pais) => {
    return pais;
}


</script>


<style scoped>
</style>