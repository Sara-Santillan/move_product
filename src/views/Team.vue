<template lang="pug">

section.team-member-view
    p Get to know your future team
    ul.team-member-list
        li.team-member(v-for="(teamMember, index) in teamMembers" :key="index")
            p {{ teamMember.title }}
    //TeamMemberList(v-bind:teamMembers="teamMembers.value")

</template>

<script>

// import TeamMemberList from '@/components/TeamMemberList.vue'
import { ref } from 'vue'

export default {
    name: 'Team',
    components: {
        // TeamMemberList
    },
    setup () {
        // const teamMembers = ref([])
        const teamMembers = ref([
            { title: 'Task 1', completed: true },
            { title: 'Task 2', completed: false }
        ])

        return {
            teamMembers
        }
    }
}

</script>

<style scoped lang="stylus">

section.team-member-view
    padding-top: 2rem
    border-top: 4px dashed #c3c3c3

</style>
