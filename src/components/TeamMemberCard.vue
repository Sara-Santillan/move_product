<template lang="pug">

ul.team-member-card
    li
        img(:src="team_member.picture.medium")
    li
        h3 {{ team_member.name.first }} {{ team_member.name.last }}
    li
        a(:href="'mailto:' + team_member.email") {{ team_member.email }}
    li
        p {{ team_member.location.country }}
    li
        button Connect now

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

ul.team-member-card
    width: 16rem
    display: flex
    flex-flow: wrap column
    justify-content: space-evenly
    border: 4px solid #000000
    img
        border-radius: 50%
        margin-top: 2rem
    p,a
        padding-top: 1rem
        font-size: 0.8rem
    button
        margin: 2rem 0

</style>
