<template lang="pug">
#nav
    router-link(to="/") go_home
router-view
</template>

<style lang="stylus">
@import url('https://fonts.googleapis.com/css2?family=Red+Hat+Text:wght@500&display=swap')
@import url('https://fonts.googleapis.com/css2?family=Red+Hat+Text:wght@700&display=swap')

body
    background-color       : #f2f2f2
    font-family            : "Red Hat Text", sans-serif
    font-weight            : 500

#app
    -webkit-font-smoothing : antialiased
    -moz-osx-font-smoothing: grayscale
    text-align             : center
    color                  : #000000
    margin-top             : 60px

a
    text-decoration        : none
    color                  : #000000
a:hover
    text-decoration        : underline
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
