<script>

    export default {
        name: 'PageFooter',

        props: {
            links: Array,
            logo: Array,
            slogan: Array,
            buttons: Array,
            mentions: Array,
            icons: Array,
        }    
    }
</script>

<template>
    <footer>

        <div class="upper-footer">
            <div class="footer-title">
                <h1>{{ slogan[3] }}</h1>

                <div class="underliner-footer"></div>

                <h3> {{ slogan[1] }} {{ slogan[2] }}</h3>

                <button class="transparent-button"> {{ buttons[3] }} </button> <button class="transparent-button"> {{ buttons[1] }} </button>
            </div> 
        </div>
        
        
        <div class="logo-container">
            <img :src="logo[1]" class="logo-footer" alt="">  
        </div>

            

        <div class="bottom-footer">
            <div class="mentions">
                <span>{{ mentions[0] }} | {{ mentions[1] }} | {{ mentions[2] }}</span>
            </div>

            <div class="social">
                <i v-for="(icon, index) in icons" :key="index" :class="icon"></i>
            </div>
        </div>
    </footer>
        
</template>

<style scoped lang="scss">
    .upper-footer {
        background-image: url(../assets/home-footer.jpg);
        background-position: center;
        background-size: cover;
        height: 500px;
    }
    .footer-title {
        text-align: center;
        padding-top:8rem;
        color: white;
        width: 60%;
        margin: auto;

            h3 {
                font-weight: lighter;
            }
    }

    .underliner-footer {
        border: solid 1px var(--my_goldenrod);
        width: 200px; 
        margin: 2rem 0 2rem 40%;
    }

    button {
        margin-top: 2rem;
        margin-right: 1rem;

         &:hover {
            cursor: pointer;
         }
    }

    .logo-container {
        margin: 20px;
        text-align: center;

        img {
            height: 50px;
        }
    }

    .bottom-footer {
        background-color: rgb(230, 228, 228);
        text-align: center;
    }

    .mentions {
        font-size: 12px;
        color: var(--edward);
        padding-top: 2rem;
    }

    .social {
        color: var(--my_goldenrod);
        font-size: 2rem;

            i {
                margin: 1rem 5px;
            }
    }
  
</style>