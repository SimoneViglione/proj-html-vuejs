<script>
    import SectionMission from './SectionMission.vue'
    import SectionValues from './SectionValues.vue'
    import SectionCauses from './SectionCauses.vue';
    import SectionArticles from './SectionArticles.vue';


    export default {
        name: 'PageMain',   
        components: { SectionMission, SectionValues, SectionCauses, SectionArticles,},
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

        <SectionCauses />

        <SectionArticles />
        
    </main>
</template>

<style scoped lang="scss">
    
</style>