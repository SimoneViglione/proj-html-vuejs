<script>
    export default {
        name: 'SectionValues',   
        props: {
            buttons: Array,
            slogan: Array
        },
        
        data() {
            return {
                
            }
        }
    }
</script>

<template>
    <section id="values">
            <div class="value-header">
                <h1>OUR VALUES</h1>

                <div></div>

                <h3> {{ slogan[2] }}</h3>
            </div>

            <div>
                <div>
                    <i class="fa-solid fa-droplet"></i>
                    <h2>Clean Water</h2>
                </div>
                <div>
                    <i class="fa-solid fa-stethoscope"></i>
                    <h2>Vaccination</h2>
                </div>
                <div>
                    <i class="fa-solid fa-graduation-cap"></i>
                    <h2>Education</h2>
                </div>
                <div>
                    <i class="fa-brands fa-pagelines"></i>
                    <h2>Farming</h2>
                    <p>Nullam convallis, orci in congue aliquet, diam mauris
                        cursus urna, Id maximus lectus magna maximus.</p>
                </div>

            </div>
        </section>
</template>

<style scoped lang="scss">
    #values {
        background-image: url(../assets/home-main.jpg);

        .value-header {

            div {
                border: solid 2px var(--my_goldenrod);
                width: 150px;
            }
        }
    }
</style>