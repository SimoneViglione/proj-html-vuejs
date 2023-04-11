<script>
    export default {
        name: 'PageHeader',
        props: ['nav'],

        data() {
            return {
            }
        }
    }
</script>

<template>
    <div class="jumbotron">
        <div class="header-nav">
            <img src="../img/avada-charity-logo.png" alt="avada logo" class="logo-header">

            <ul>
                <li v-for="(item, index) in nav.headerNav" :key="index">{{ item }}</li>
            </ul>
        </div>

        <div class="slogan">
            <h1>MAKE A DIFFERENCE</h1>
            <p>As long as poverty, injustice & inequality persist, none of us can truly rest</p>
            <button class="transparent-button"> OUR MISSION </button>
            <button class="transparent-button"> DONATE NOW </button>
        </div>
    </div>
</template>

<style>
    .jumbotron {
        background-image: url(../img/home-page-slider.jpg);
        background-size: cover;
        height: 700px;
        color: white;
    }

    .logo-header {
        margin: 2rem 5rem;
        height: 50px;
    }

    .slogan {
        text-align: center;
        margin-top: 12rem;
    }
</style>