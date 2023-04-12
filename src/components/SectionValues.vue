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
      
            <div class="value-header">
                
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

        .value-header {
            padding-top: 3rem;
            text-align: center;

            .underliner {
                border: solid 2px var(--my_goldenrod);
                width: 150px;
                margin: 2rem 0 2rem 45%;
            }
        }

        .cards-container {
            display: flex;
            text-align: center;
            margin-top: 8rem;

                .cards {
                    width: calc(100% / 4);

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