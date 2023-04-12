<script>
    export default {
        name: 'SectionMission',   
        props: {
            buttons: Array,
            slogan: Array
        }    
    }
</script>

<template>
    <section id="mission">
        <div class="left">
            <h1>EVERY MOMENT COUNTS</h1>

            <div></div>

            <p>Curabitur non mi et turpis pharetra vulputate, Cras consequat. risus nec commodo vehicula, nisi est laoreet Leo. convallis nisi nibh id velit, Aliquam
                mattis metus a nisi pretium.</p>

            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ac nibh vestibulum. laoreet ipsum quis vestibulum nisi. Curabitur non mi et turpis
                pharetra vulputate. Ipsum dolor sit amet. consectetur adipiscing elit Praesent ac nibh vestibulum. laoreet ipsum quis. vestibulum nisi.</p>

            <p>Curabitur non mi et turpis pharetra vulputate. Cras consequat. risus nec commodo vehicula, nisi est laoreet leo, ac convallis nisi nibh id velit.</p>

            <a class="yellow-button"> {{ buttons[0] }} </a>
        </div>

        <div class="right">
            <div class="goal-wrapper">
                <div class="right-goals">
                    <i class="fa-regular fa-heart"></i>
                    <h1>2032</h1>
                </div>
                
                <h2> Volunteers Worldwide </h2>
            </div>
            <div class="goal-wrapper">
                <div class="right-goals">
                    <i class="fa-solid fa-globe"></i>
                    <h1>132</h1>
                </div>
                
                <h2> Active Projects </h2>
            </div>

            <div class="goal-wrapper">
                <div class="right-goals">
                    <i class="fa-regular fa-dollar-sign"></i>
                    <h1>3.8M</h1>
                </div>
                
                <h2> Donated </h2>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
     #mission {
        display: flex;
        height: 500px;


        .right {
            width: 30%;
            height: 100%;
            background-image: url(../assets/red-bg.jpg);
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 2.5rem;

                .right-goals {
                    display: flex;
                    align-items: center;
                    justify-content: center;

                    
                        i {
                            align-self: center;
                            font-size: 2rem;
                            margin-right: 5px;
                        }

                        h1 {
                            font-size: 2.2rem;
                    
                        }

                        
                }

                h2 {
                    font-size: 1rem;
                    
                        &:last-child{
                            margin-left: 15px;
                        }
                }
        }

        .left {
            width: 70%;

                h1 {
                    margin-top: 5rem;
                    margin-left: 7rem;
                    font-size: 2rem;
                }

                p {
                    margin-left: 7rem;
                    margin-bottom: 1rem;
                    font-size: 0.8rem;
                    color: var(--tuna);
                }

                a {
                    margin-left: 7rem;
                    margin-top: 2rem;
                    display: block;
                    width: 140px;
                }

                div {
                    border: solid 2px var(--my_goldenrod);
                    margin: 2rem 0 3rem 7rem;
                    width: 180px;
                }
        }
    } #mission {
        display: flex;
        height: 500px;


        .right {
            width: 30%;
            height: 100%;
            background-image: url(../assets/red-bg.jpg);
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 2.5rem;

                .right-goals {
                    display: flex;
                    align-items: center;
                    justify-content: center;

                    
                        i {
                            align-self: center;
                            font-size: 2rem;
                            margin-right: 5px;
                        }

                        h1 {
                            font-size: 2.2rem;
                    
                        }

                        
                }

                h2 {
                    font-size: 1rem;
                    
                        &:last-child{
                            margin-left: 15px;
                        }
                }
        }

        .left {
            width: 70%;

                h1 {
                    margin-top: 5rem;
                    margin-left: 7rem;
                    font-size: 2rem;
                }

                p {
                    margin-left: 7rem;
                    margin-bottom: 1rem;
                    font-size: 0.8rem;
                }

                a {
                    margin-left: 7rem;
                    margin-top: 2rem;
                    background-color: var(--my_goldenrod);
                    padding: 8px 15px;
                    color: white;
                    font-size: 0.9rem;
                    display: block;
                    width: 140px;
                }

                div {
                    border: solid 2px var(--my_goldenrod);
                    margin: 2rem 0 3rem 7rem;
                    width: 180px;
                }
        }
    }
</style>