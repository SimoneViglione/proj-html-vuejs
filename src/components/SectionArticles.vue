<script>
    export default {
        name: 'SectionArticles',

        data() {
            return {
                articles: [
                    {
                        path: 'src/assets/article-1.jpg',
                        title: 'Understanding community complexities',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-2.jpg',
                        title: 'Farmers Making Difference',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-3.jpg',
                        title: 'Sustainable trade tactics',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-4.jpg',
                        title: 'Meeting remote tribes in Peru',
                        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis dolor, eum quam corporis rerum neque.',
                    },
                    {
                        path: 'src/assets/article-5.jpg',
                        title: 'The human story of Uniqueness',
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

            <div class="articles-underliner"></div>

            <h3> Together we make all the difference </h3>

            <div class="articles-gallery">
                

                <div class="first-image" v-if="articles.length > 0">
                    <img :src="articles[0].path" />
                    <div class="first-article-description">
                        <h2> {{ articles[0].title }} </h2>
                        <p>{{ articles[0].description }}</p> 
                    </div>
                    
                </div>

                <div class="other-images" v-if="articles.length > 1">
                    <div v-for="(article, index) in articles.slice(1)" :key="index" class="other-images-container">
                        <img :src="article.path" />
                        <div class="article-description">
                            <h4>{{ article.title }}</h4>
                            <p>{{ article.description }}</p> 
                        </div>
                        
                    </div>
                </div>
            </div>
        </div>

        <div class="banner">
            <h4>VIEW ALL OUR ARTICLES</h4>
        </div>
    
    </section>
</template>

<style scoped lang="scss">
    #articles {
        padding-top: 5rem;
        width: 70%;
        margin: auto;
        height: 1000px;
        
    }

    .articles-underliner {
        border: solid 1px var(--my_goldenrod);
        width: 200px; 
        margin: 2rem auto;
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
        height: 700px;
        display: flex;
        margin-top: 3rem;
        text-align: start;

            p {
                color: var(--tuna);
            }
    }

    .first-image {

        margin-right: 40px;

        img {
            height: 400px;
            margin-bottom: -5px;
        }

        h2 {
            color: var(--my_goldenrod);
            padding-left: 1rem;
        }

    }

    .first-article-description {
        border: solid 1px rgba(128, 128, 128, 0.363);
        border-top: none;

        padding-top: 1rem;

            p {
                padding: 1rem 1rem;
            }
    }

    .other-images {
        
        img {
            height: 112px;
        }
    }

    .other-images-container {
        display: flex;
        margin-bottom: 20px;
        
    }

    .article-description {
        padding-left: 20px;

            h4 {
                color: var(--my_goldenrod);
            }
    }

    .banner {
        background-color: var(--sienna);
        color: white;
        padding: 15px 0;
        margin-bottom: 5rem;
        text-align: center;

        &:hover {
            background-color: rgb(44, 152, 164);
            cursor: pointer;
        }
    }
</style>