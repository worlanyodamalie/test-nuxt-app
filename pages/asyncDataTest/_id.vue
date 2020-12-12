<template>
    <div>
        <div class="flex ">
            <h1>{{ post.title }}</h1>
            <nuxt-link to="/asyncDataTest">Back to list</nuxt-link>
        </div>       
        <div>
            <h2>{{ post.body }}</h2>
        </div>
        
    </div>
</template>
<script>
export default {
    async asyncData({params ,$http}){
       const post = await $http.$get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
       return { post }
    }
}
</script>