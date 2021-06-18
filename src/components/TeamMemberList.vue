<template lang="pug">
section
    h2 TeamMemberList
    ul.team-member-list
        li.team-member(v-for="(member, index) in members" :key="index" :member="member")
            TeamMemberCard(v-bind:member="member")
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
.team-member-list
    width: 9rem
    margin: auto
</style>
