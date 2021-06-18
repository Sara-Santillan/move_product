<template lang="pug">
</template>

<script>
import TeamMemberCard from './TeamMemberCard.vue'

export default {
    name: 'TeamMemberList',
    props: {
        members: {
            type: Array,
            required: true
        }
    },
    components: {
        TeamMemberCard
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
</style>
