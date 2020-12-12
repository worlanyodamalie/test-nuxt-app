<template>
 <div>
    <!-- <h1>{{title}}</h1> -->
    <nuxt-link to="/asyncDataTest" > Blog </nuxt-link>
    <nav-header/>
    <quotes/>
    <cards/>
 </div>   
</template>

<script>
import NavHeader from "~/components/NavHeader.vue";
import Quotes from "~/components/Quotes.vue";
import Cards from "~/components/Cards.vue";
export default {
   components: {
     NavHeader,
     Quotes,
     Cards
   },
   asyncData (context){
      return { title: 'async data'}
   } 
}
</script>


