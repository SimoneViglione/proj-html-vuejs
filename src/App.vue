<script>
    import PageHeader from './components/PageHeader.vue'
    import PageMain from './components/PageMain.vue'
    import PageFooter from './components/PageFooter.vue'

    export default {
        name: 'App',
        components: {PageHeader, PageMain, PageFooter},

        data() {
            return {
                links: ["HOME", "MISSION", "CAUSES", "JOURNAL", "DONATE"],
                logo: ["/logo.png", "/logo-footer.png"],
                slogan: ["MAKE A DIFFERENCE", "As long as poverty, injustice & inequality persist, none of us can truly rest", "lt doesnt take much to change a life. Get in touch today and start making the difference.", "CHANGE A LIFE TODAY"],
                buttons: ["OUR MISSION", "DONATE NOW", "LEARN MORE", "VOLUNTEER"],
                mentions: ["© Copyrigth 2012 - 2020 AVADA THEME BY THEME FUSION", "ALL RIGHTS RESERVED", "POWERED BY WORDPRESS"],
                icons: ["fa-brands fa-facebook", "fa-brands fa-instagram", "fa-brands fa-twitter", "fa-brands fa-youtube"]
            }
        }
    }
</script>

<template>
    <header>
        <PageHeader :links="links" :logo="logo" :slogan="slogan" :buttons="buttons"/>

        <PageMain :buttons="buttons" :slogan="slogan"/>

        <PageFooter :buttons="buttons" :slogan="slogan" :logo="logo" :mentions="mentions" :icons="icons"/>
    </header>
</template>

<style lang="scss">
    @use "./styles/general.scss";
</style>
