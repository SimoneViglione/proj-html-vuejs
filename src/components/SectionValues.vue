<script>
    export default {
        name: 'SectionValues',   
        props: {
            buttons: Array,
            slogan: Array
        },
        
        data() {
            return {
                values: [
                {
                    name: 'Clean Water',
                    icon: 'fa-solid fa-droplet',
                    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
                },
                {
                    name: 'Vaccination',
                    icon: 'fa-solid fa-stethoscope',
                    description: 'Praesent aliquet enim ac lacus tincidunt, vel tempus lorem consequat.'
                },
                {
                    name: 'Education',
                    icon: 'fa-solid fa-graduation-cap',
                    description: 'Fusce non feugiat nunc, a luctus elit. Ut elementum elit quis imperdiet ultricies.'
                },
                {
                    name: 'Farming',
                    icon: 'fa-brands fa-pagelines',
                    description: 'Nullam convallis, in aliquet, diam cursus urna, id maximus lectus magna maximus.'
                }
                ]
            }
        }
    }
</script>

<template>
    <section id="values">
      
            <div class="value-title">
                
                <h1>OUR VALUES</h1>

                <div class="underliner"></div>

                <h3> Think Big. Act Bigger</h3>
            </div>

            <div class="cards-container">
                <div v-for="(value, index) in values" :key="index" class="cards">
                    <i :class="value.icon"></i>
                    <h1>{{ value.name }}</h1>
                    <p>{{ value.description }}</p>
                    <a class="yellow-button"> {{ buttons[2] }}</a>
                </div>
            </div>
       
    </section>
</template>

<style scoped lang="scss">
    #values {
        background-image: url(../assets/home-main.jpg);
        background-size: cover;
        color: white;
        height: 700px;

        .value-title {
            padding-top: 3rem;
            text-align: center;

                h1 {
                    letter-spacing: 3px;
                }
        }

        .cards-container {
            display: flex;
            justify-content: center;
            text-align: center;
            padding-top: 8rem;
            margin: auto;

            .cards {
                width: calc((100% / 4) - 3rem);

                    &:hover {

                        cursor: pointer;

                        i {
                            color: rgb(36, 136, 139);
                        }

                        a {
                            border: solid 2px white;
                            background-color: rgb(36, 136, 139);
                        }
                        
                    }

                i {
                    font-size: 4rem;
                    color: var(--my_goldenrod);
                }

                h1 {
                    margin: 2rem 0;
                }

                p{
                    margin: 2rem 0;
                    color: var(--french);
                }
            }
        }
    }
</style>