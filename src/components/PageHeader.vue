<script>
    export default {
        name: 'PageHeader',
        props: {
            links: Array,
            logo: String,
            slogan: Array,
            buttons: Array
        }    
    }
</script>

<template>
    <div class="jumbotron">
        <div class="header-nav">
            <img :src="logo" class="logo-header" alt="Logo">
            <ul>
                <li v-for="link in links" :key="link">{{ link }}</li>
            </ul>
        </div>

        <div class="slogan">
            <h1>{{ slogan[0] }}</h1>
            <p>{{ slogan[1] }}</p>
            <button class="transparent-button"> {{ buttons[0] }} </button> <button class="yellow-button"> {{ buttons[1] }} </button>

        </div>
    </div>
</template>

<style scoped lang="scss">
    .jumbotron {
        background-image: url(../assets/home-header.jpg);
        background-size: cover;
        height: 710px;
        color: white;
        width: 100%;
    }

    .header-nav {
        display: flex;
        padding-top: 3rem;
        height: 100px;
        align-items: center;

            ul {
                display: flex;
                gap: 2rem;
                margin-left: 40%;
                align-items: center;
            }
    }

    li:last-child {
        color: white;
        background-color: var(--my_goldenrod);
        padding: 5px 15px;

         &:hover {
            color: black;
         }
        
    }

    li:hover {
        color: var(--my_goldenrod);
        cursor: pointer;
    }

    .logo-header {
        margin-left: 5rem;
        height: 50px;
    }

    .slogan {
        text-align: center;
        margin-top: 14rem;

        h1 {
                font-size: 3rem;
            }

        p {
            margin-top: 1rem;
            color: rgba(255, 255, 255, 0.75);
        }
    }

    button {
        margin-top: 2rem;

         &:hover {
            cursor: pointer;
         }
    }

    button:last-child {
        color: var(--my_goldenrod);
        border: var(--my_goldenrod) solid 2px;

            &:active {
                color: black;
            }
    }

</style>