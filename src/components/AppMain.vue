<template>
    <main>
        <section id="network">
            <div class="network container">
                <div class="row">
                    <div class="col-6">
                        <p>About the Network</p>
                        <h2><span>The</span> Company</h2>
                        <p class="text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eius nisi ullam rerum reprehenderit, temporibus numquam provident</p>
                        <p class="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem, dolorum harum? Maiores, fugit. Quasi ab ipsa, ad quibusdam in cupiditate!</p>
                    </div>
                    <div class="col-6">
                        <div class="info">
                            <i class="fa-solid fa-award"></i> <span>Tradition</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                        <div class="info">
                            <i class="fa-solid fa-lock"></i> <span>Security</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                        <div class="info">
                            <i class="fa-regular fa-pen-to-square"></i> <span>Certificate</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                        <div class="info">
                            <i class="fa-solid fa-graduation-cap"></i> <span>Expertise</span>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script>
export default {
    name: 'AppMain',
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';
#network{
    background-color: $main-dark-bg;
    width: 100%;
}
.row{
    padding: 90px 0;
}
.col-6{
    color: white;
        p{
            color: $green-font;
            font-size: 18px;
            margin-bottom: 30px;
        }
        h2{
            font-size: 56px;
            font-weight: 900;
            margin: 0;
            margin-bottom: 10px;
                span{
                    background-color: $dark-green-bg;
                    border-radius: 5px;
                    padding: 0px 25px;
                }
        }
        .text{
            color: $lightgrey-font;
            font-size: 18px;
            margin: 20px 0;
        }
}
.info{
    width: 50%;
    display: inline-block;
    padding: 10px 20px;

        .fa-solid,.fa-regular{
            color: $green-font;
            font-size: 20px;
        }
        span{
            font-size: 30px;
            font-weight: 700;

        }
        p{
            color: $lightgrey-font;
            margin-top: 20px;
        }
}
</style>