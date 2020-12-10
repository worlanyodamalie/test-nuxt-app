<template>
    <div class="quotes flex flex-column center w-50 ba bw1">
           <p class="f1 san-serif" v-if="$fetchState.pending">Fetching quote...</p>
           <p class="f1 san-serif" v-else-if="$fetchState.error">An error occured</p>
           <h1 v-else class="f2 pt3 pb3 pl5 pr5 courier">{{quotes.value}}</h1>
           <button @click="$fetch" class="w-20 center pa2 mb2 san-serif">More</button>
    </div>
</template>

<script>
export default {
   data() {
       return {
           quotes: []
           }
   },
   async fetch() {
      var quote = await fetch('https://api.chucknorris.io/jokes/random').then(
           res => res.json()
       )
       this.quotes = quote ;
   }
}
</script>
