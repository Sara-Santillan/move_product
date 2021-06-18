<template lang="pug">
ul
    li {{ member.name.first }}
    li {{ member.name.last }}
br
</template>

<script>
export default {
    name: 'TeamMemberCard',
    props: {
        member: {
            type: Object,
            required: true
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
</style>
