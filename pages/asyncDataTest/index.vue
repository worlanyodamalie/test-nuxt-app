<template>
    <div>
        <h1>Blog posts</h1>
        <nuxt-link to="/" > Home </nuxt-link>
        <div v-if="posts && posts.length">
            <div v-for="post in posts" 
                 :key="post.id">
                <nuxt-link :to="`/asyncDataTest/${post.id}`"> {{post.title}} </nuxt-link>
            </div>

        </div>
    </div>
</template>
<script>
export default {
    async asyncData({$http}){
        const posts = await $http.$get(`https://jsonplaceholder.typicode.com/posts`)
       return {
             posts
        }
    }
}
</script>