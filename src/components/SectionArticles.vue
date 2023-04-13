<script>
    export default {
        name: 'SectionArticles',

        data() {
            return {
                articles: [
                    {
                        path: 'src/assets/article-1.jpg',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-2.jpg',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-3.jpg',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-4.jpg',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-5.jpg',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                ]
            }
        },
        
    }
</script>

<template>
    <section id="articles">
        <div class="articles-title">
            <h1>LATEST ARTICLES</h1>

            <div class="underliner"></div>

            <h3> Together we make all the difference </h3>

            <div class="articles-gallery">
                
                <div class="articles-gallery">
                    <div v-for="article in articles" :key="article.path" >
                        <img :src="article.path" />
                        <p>{{ article.description }}</p>
                    </div>
                </div>

            </div>

            <div class="banner">
                <h4>VIEW ALL OUR ARTICLES</h4>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    #articles {
        padding-top: 5rem;
        width: 70%;
        margin: auto;
        
    }

    .articles-title {
        text-align: center;
        margin-top: 8rem;

            h1 {
                letter-spacing: 2px;
            }

            h3 {
                color: var(--tuna);
            }
    }

    .articles-gallery {
        height: 400px;
        display: flex;

            img {
                height: 200px;
            }
    }

    .banner {
        background-color: var(--sienna);
        color: white;
        padding: 15px 0;
        margin-bottom: 5rem;
    }
</style>