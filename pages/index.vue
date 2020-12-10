<template>
 <div>
    <nav-header/>
    <cards/>
 </div>   
</template>

<script>
import NavHeader from "~/components/NavHeader.vue";
import Cards from "~/components/Cards.vue"
export default {
   components: {
     NavHeader,
     Cards
   } 
}
</script>


