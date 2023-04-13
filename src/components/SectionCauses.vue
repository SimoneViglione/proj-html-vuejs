<script>
     export default {
        name: 'SectionCauses',

        data() {
            return {
                images: [
                {
                    path: 'src/assets/fair-trade.jpg',
                    title: 'Fair Trade'
                },
                {
                    path: 'src/assets/shelter.jpg',
                    title: 'Shelter'
                },
                {
                    path: 'src/assets/farming.jpg',
                    title: 'Farming'
                },
                {
                    path: 'src/assets/vaccines.jpg',
                    title: 'Vaccines'
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
                <div class="image-wrapper" v-for="(image, index) in images" :key="index">
                    <img :src="image.path" alt="image">
                    <h3>{{ image.title }}</h3> 
                </div>
                
            </div>

            <div class="banner">
                <h1>VIEW ALL OUR CAUSES</h1>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    .causes-title {
        text-align: center;
        margin-top: 3rem;

            h1 {
                letter-spacing: 2px;
            }

            h3 {
                color: var(--tuna);
            }
    }

    .gallery {
        display: flex;
        margin-top: 6rem;
        gap: 10px;

        .image-wrapper {
            margin: auto;
            position: relative;

            &:hover {
                h3 {
                    display: block;
                    
                }

                &::before {
                    content: "";
                    position: absolute;
                    top: 0;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    background-color: var(--sienna-transparent);
                }
            }



            h3 {
                display: none;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                color: white;
            }
        }

        img {
            height: 250px;
        }
    }

    .banner {
        margin-top: 100px;
        height: 150px;
        width: 100%;
        background-color: var(--sienna);
        display: flex;  
        justify-content: center;
        align-items: center;

            &:hover {
                background-color: rgb(23, 145, 172);
                cursor: pointer;
            }

            h1 {
                color: white;
            }
    }
</style>