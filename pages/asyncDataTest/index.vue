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
    //using nuxt/http for http request
    // async asyncData({$http}){
    //     const posts = await $http.$get(`https://jsonplaceholder.typicode.com/posts`)
    //    return {
    //          posts
    //     }
    // }

    //using nuxt/axios for http requests
    async asyncData({$axios}){
        const posts = await $axios.$get(`https://jsonplaceholder.typicode.com/posts`)
        return {
            posts
        }
    }


}
</script>