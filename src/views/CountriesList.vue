<template>
    <div class="container" style="height: calc(100vh - 52px);">
        <div class="columns mt-0" style="height: 100%" >
            <div class="column is-4" style="overflow: auto">

                    <router-link v-for="country in countries" :to="{name:'details', params:{code: country.alpha3Code}}" class="media is-clickable" >
                        <img :src="`https://flagpedia.net/data/flags/icon/72x54/${country.alpha2Code.toLowerCase()}.png`" />
            
                        <div class="media-content">
                            <h1>{{country.name.common}}</h1> 
                        </div>
                    </router-link>
                    
                </div> 
        </div>
    </div>


</template>
<script setup>
import countries from '../assets/countries.json'
import CountryDetails from './CountryDetails.vue';


</script>
<style scoped>
.container{
    padding:5px 20px
}
.column{
    background-color: aquamarine;
    
}

</style>