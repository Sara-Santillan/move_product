<template lang="pug">
section.team-member-view
    p Get to know your future team
    TeamMemberList(v-bind:team_members="team_members")
</template>

<style scoped lang="stylus">

section.team-member-view
    padding-top: 2rem
    border-top: 4px dashed #c3c3c3
</style>

<script>
import TeamMemberList from '@/components/TeamMemberList.vue'

export default {
    name: 'Team',
    components: {
        TeamMemberList
    },
    // we will add methods to FETCH data from an API &
    // pass it into data, to execute in the setup hook:
    data () {
        return {
            team_members: []
        }
    },
    methods: {
        async fetchMembers () {
            const url = 'https://randomuser.me/api/?results=4'
            await fetch(url)
                .then(response => response.json())
                .then(data => {
                    this.team_members = data.results
                })
        }
    },
    mounted () {
        this.fetchMembers()
    }
}
</script>
