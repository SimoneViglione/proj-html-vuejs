<script>
    export default {
        name: 'PageMain',   
    }
</script>

<template>
    <section id="mission">
        <div class="left">

        </div>

        <div class="right">

        </div>
    </section>
</template>

<style scoped lang="scss">
    #mission {
        display: flex;
        height: 500px;


        .right {
            width: 30%;
            border: solid 1px red;
        }

        .left {
            width: 70%;
            border: solid 1px yellow;
        }
    }


</style>