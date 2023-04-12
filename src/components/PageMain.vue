<script>
    import SectionMission from './SectionMission.vue'
    import SectionValues from './SectionValues.vue'

    export default {
        name: 'PageMain',   
        components: {SectionMission, SectionValues},
        props: {
            buttons: Array,
            slogan: Array
        }    
    }
</script>

<template>
    <main>
        <SectionMission :buttons="buttons" slogan="slogan"/>

        <SectionValues :buttons="buttons" slogan="slogan"/>
        
    </main>
</template>

<style scoped lang="scss">
    
</style>