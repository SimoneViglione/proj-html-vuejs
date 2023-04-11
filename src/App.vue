<script>
    import PageHeader from './components/PageHeader.vue'

    export default {
        name: 'App',
        components: {PageHeader},

        data() {
            return {
                headerMenu: [
                    {
                        "logo": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                        "headerNav": ["HOME", "MISSION", "CAUSES", "JOURNAL", "DONATE"]
                    }
                ]
            }
        }
    }
</script>

<template>
    <header>
        <PageHeader :nav="headerMenu"/>
    </header>
</template>

<style lang="scss">
    @use "./styles/general.scss";
</style>
