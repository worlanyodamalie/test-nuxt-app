<template>
    <div class="flex flex-wrap justify-center">
        <article v-for="cardItem in cardItems" :key="cardItem.title" v-tooltip="'This is a card'" class="mw5 pa3 ma4 br3 bg-gray washed-blue">
            <div class="tc">
                <img :src="cardItem.image" class="h4 w4 dib ba b--black-05 pa2"  :class="[cardItem.title === 'Cat' ? 'br-100' :  '']">
                <h1 class="f3">{{cardItem.title}}</h1>
                <h1 class="f5">{{cardItem.description}}</h1>
            </div>
        </article>    
    </div>
</template>
<script>
export default {
    data(){
        return {
           cardItems: [
               {
                   image: 'http://tachyons.io/img/avatar_1.jpg',
                   title: 'Cat',
                   description: 'The cat is a domestic species of small carnivorous mammal. It is the only domesticated species in the family Felidae and is often referred to as the domestic cat to distinguish it from the wild members of the family.'
               },
               {
                   image: 'http://tachyons.io/img/logo.jpg',
                   title: 'Rounded Medium',
                   description: 'This image has rounded edges.'
               }

           ]
        }
    }
}
</script>