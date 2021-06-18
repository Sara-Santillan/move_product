<template lang="pug">
.about
    h1 This is the team view
    p {{ members }}
</template>

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
            members: []
        }
    },
    methods: {
        async fetchMembers () {
            const url = 'https://randomuser.me/api/?results=4'
            await fetch(url)
                .then(response => response.json())
                .then(data => {
                    this.members = data.results
                })
        }
    },
    mounted () {
        this.fetchMembers()
    }
}
</script>
