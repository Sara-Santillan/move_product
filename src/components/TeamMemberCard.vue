<template lang="pug">
ul.team-member-card
    li {{ team_member.name.first }}
    li {{ team_member.name.last }}
br
</template>

<script>
export default {
    name: 'TeamMemberCard',
    props: {
        team_member: {
            type: Object,
            required: true
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">

</style>
