<template>
    <div>
        <ul v-for="country in countries">
            <li>
            <router-link :to="{name:'details', params:{alpha3Code:country.alpha3Code}}">
                    <h1>{{country.name.common}}</h1> 
                    <img :src="`https://flagpedia.net/data/flags/icon/72x54/${country.alpha2Code.toLowerCase()}.png`" />
                </router-link>
            </li> 
        </ul>
    </div>


</template>
<script setup>
import countries from '../assets/countries.json'
import CountryDetails from './CountryDetails.vue';
</script>
<style scoped>

</style>