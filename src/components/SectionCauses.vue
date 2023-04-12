<script>
     export default {
        name: 'SectionCauses',

        data() {
            return {
                images: [
                {
                    path: 'src/assets/fair-trade.jpg',
                },
                {
                    path: 'src/assets/shelter.jpg',
                },
                {
                    path: 'src/assets/farming.jpg',
                },
                {
                    path: 'src/assets/vaccines.jpg',
                }
                ]
            }
        }
    }
</script>

<template>
    <section id="causes">
        <div class="causes-title">
            <h1>RECENT CAUSES</h1>

            <div class="underliner"></div>

            <h3> We run projects in over 30 countries in 5 contintents </h3>

            <div class="gallery">
                <img v-for="(image, index) in images" :key="index" :src="image.path" alt="image">
            </div>

            <div class="banner">
                <h3>VIEW ALL OUR CAUSES</h3>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">

    #causes {
        height: 600px;
    }
    .causes-title {
        text-align: center;
        margin-top: 3rem;
    }

    .gallery {
        display: flex;
        margin-top: 6rem;

        img {
            height: 200px;
            margin: auto;
        }
    }

    .banner {
        margin-top: 100px;
        height: 100px;
        width: 100%;
        background-color: var(--sienna);
        color: white;
        display: flex;  
        justify-content: center;
        align-items: center;
    }
</style>