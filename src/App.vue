<template lang="pug">
#nav
    router-link(to="/") go_home
router-view
</template>

<style lang="stylus">
#app
    font-family            : Roboto, Helvetica, Arial, sans-serif
    -webkit-font-smoothing : antialiased
    -moz-osx-font-smoothing: grayscale
    text-align             : center
    color                  : #2c3e50
    margin-top             : 60px
</style>

<script>
// @ is an alias to /src
import Home from '@/views/Home.vue'

export default {
    name: 'app',
    components: {
        Home
    }
}
</script>
