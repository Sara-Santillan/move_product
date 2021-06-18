<template lang="pug">
h1 we move_product
p Design.
p Develop.
p Deploy.
br
router-link(to="/team") Meet the team
<br>
router-link(to="/product") Try our apps
br
br
button Start free trial
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
    name: 'Home',
    components: {
    }
}
</script>
