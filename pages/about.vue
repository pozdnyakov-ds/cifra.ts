<template>
    <div>
        <ul>
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li>About page</li>
        <li><button @click="console.log('Push me...')">Push me</button></li>
        </ul>
    </div>
</template>

<script>
// import { useRouter, useRoute } from '@nuxtjs/composition-api'
    
export default {
    // setup() { 
    //     const pushMe = () => { 
    //         console.info("onClick...")
    //     }

    //     const router = useRouter()

    //     return {
    //         pushMe
    //     }
    // }    
}
</script>

<style scoped>

</style>