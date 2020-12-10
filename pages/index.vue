<template>
 <div>
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
   } 
}
</script>


