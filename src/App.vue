<script>
    import PageHeader from './components/PageHeader.vue'
    import PageMain from './components/PageMain.vue'

    export default {
        name: 'App',
        components: {PageHeader, PageMain},

        data() {
            return {
                links: ["HOME", "MISSION", "CAUSES", "JOURNAL", "DONATE"],
                logo: "../public/logo.png",
                slogan: ["MAKE A DIFFERENCE", "As long as poverty, injustice & inequality persist, none of us can truly rest"],
                buttons: ["OUR MISSION", "DONATE NOW"]
            }
        }
    }
</script>

<template>
    <header>
        <PageHeader :links="links" :logo="logo" :slogan="slogan" :buttons="buttons"/>

        <PageMain/>
    </header>
</template>

<style lang="scss">
    @use "./styles/general.scss";
</style>
