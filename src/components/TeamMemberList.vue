<template lang="pug">
section
    h2 TeamMemberList
    ul.team-member-list
        li.team-member(v-for="(team_member, index) in team_members" :key="index" :team-member="team_member")
            TeamMemberCard(v-bind:team_member="team_member")
</template>

<script>
import TeamMemberCard from './TeamMemberCard.vue'

export default {
    name: 'TeamMemberList',
    props: {
        team_members: {
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
