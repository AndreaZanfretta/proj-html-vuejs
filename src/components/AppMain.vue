<template>
    <main>
        <section id="network">
            <div class="container">
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
        <section id="services">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <p>Our Business Area</p>
                        <h2>Excellence in <span>Services</span></h2>
                        <p class="text">We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowed professionals. These are some options that you can hire.</p>
                    </div>
                    <div class="btn">
                        <a href="#">See All</a>
                    </div>
                </div>
                <div class="row row-card">
                    <div v-for="(card, index) in cards" :key="index" class="col-4">
                        <div  class="card">
                            <i class="fa-solid fa-arrow-right"></i>
                            <i :class="card.icon"></i>
                            <h3>{{card.title}}</h3>
                            <p>{{card.subTitle}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section id="management">
            <div class="row">
                    <div class="col">
                        <p>How it works in practice</p>
                        <h2><span>Process</span> Management</h2>
                        <p class="text">We work with innovative methodologies to ensure that the entire reformatting process is done from start to finish as planend</p>
                    </div>
            </div>
            <div class="row-line">
                <div class="line"></div>
                <div class="wrapper">
                    <div class="row">
                        <div v-for="(numcard, index) in management" :key="index" class="col col-line">
                            <div class="num-card">
                                <p class="circle">{{numcard.n}}</p>
                                <h3>{{numcard.title}}</h3>
                                <p>{{numcard.subTitle}}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section id="team">
            <div class="container">
                <div class="row">
                    <div class="col-9">
                        <p>We like what we do</p>
                        <h2><span>Team</span> of Experts</h2>
                        <p class="text">Ethics and integrity are the bases on which our professionals build their careers.
                        They are fundamentals that become daily attitudes.</p>
                        <div class="row row-team">
                            <div v-for="(member, index) in team" :key="index" class="col-6">
                                <div class="team-card">
                                    <img :src="require('../' + member.img + '.jpg')" alt="">
                                    <div class="text">
                                        <h3>{{member.name}}</h3>
                                        <p>{{member.role}}</p>
                                        <i class="fa-brands fa-facebook-f"></i>
                                        <i class="fa-brands fa-twitter"></i>
                                        <i class="fa-brands fa-linkedin-in"></i>
                                        
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                    </div>
                    <div class="col-3">
                        <div class="box">
                            <h3>President Speech</h3>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium explicabo autem beatae quas ratione voluptates nihil, totam debitis itaque. Doloribus maxime ex aliquam</p>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia numquam explicabo doloribus, a suscipit eveniet vero.</p>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat ab et hic perferendis cum.</p>
                            <p class="cit">T.Johnson</p>
                            <i class="fa-solid fa-quote-right"></i>
                        </div>
                    </div>
                </div>
            </div>
        </section>
         <section id="news">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <p>Our Editorial Content</p>
                        <h2>Latest <span>News</span></h2>
                        <p class="text">Every week we publish content about what is best in the business world.</p>
                    </div>
                    <div class="btn">
                        <a href="#">See All</a>
                    </div>
                </div>
                <div class="row row-news">
                    <div class="col-4">
                        <div class="img-box">
                            <img src="../assets/news-1.jpg" alt="">
                            <div class="overlay"></div>
                            <p>Increasing Creativity is possible for everyone</p>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-box">
                            <img src="../assets/news-2.jpg" alt="">
                            <div class="overlay"></div>
                            <p>Because market research is part of the business plan</p>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-box">
                            <img src="../assets/news-3.jpg" alt="">
                            <div class="overlay"></div>
                            <p>Working from home is now a trend</p>
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
    data(){
        return{
            cards: [
                {
                    icon: 'fa-solid fa-network-wired',
                    title: 'Audit & Assurance',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
                },
                {
                    icon: 'fa-solid fa-briefcase',
                    title: 'Financial Advisory',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
                },
                {
                    icon: 'fa-solid fa-chart-simple',
                    title: 'Analytics and M&A',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
                },
                {
                    icon: 'fa-solid fa-plane-departure',
                    title: 'Middle Marketing',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
                },
                {
                    icon: 'fa-solid fa-earth-europe',
                    title: 'Legal Consulting',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
                },
                {
                    icon: 'fa-solid fa-inbox',
                    title: 'Regulatory Risk',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit.',
                },
            ],
            management: [
                {
                    n: '01',
                    title: 'Collection of information',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing',
                },
                {
                    n: '02',
                    title: 'Strategic planning',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing',
                },
                {
                    n: '03',
                    title: 'Assignment of responsabilities',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing',
                },
                {
                    n: '04',
                    title: 'Formatting process',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing',
                },
                {
                    n: '05',
                    title: 'Continuity formalization',
                    subTitle: 'Lorem ipsum dolor, sit amet consectetur adipisicing',
                },
                
            ],
            team: [
                {
                    img: 'assets/team-1',
                    name: 'David Cooper',
                    role: 'CTO & CO-FOUNDER'
                },
                {
                    img: 'assets/team-3',
                    name: 'Oliver Jones',
                    role: 'CHIEF PROCUREMENT'
                },
                {
                    img: 'assets/team-2',
                    name: 'Emma Lopez',
                    role: 'CHIEF MARKETING'
                },
                {
                    img: 'assets/team-4',
                    name: 'T. Johnson',
                    role: 'CEO & PRESIDENT'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';
// section1 //
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
            font-weight: 700;
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
                font-weight: 400;
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
            font-weight: 400;
        }
}
// section2 //
#services{
background-color: $main-green-bg;
    .col{
        position: relative;
        p{
        color: $green-font;
        font-size: 18px;
        margin-bottom: 30px;
        font-weight: 700;
        }
        h2{
            font-size: 56px;
            font-weight: 900;
            margin: 0;
            margin-bottom: 10px;
                span{
                    background-color: $ligthgreen-bg;
                    color: $btn-green-bg;
                    border-radius: 5px;
                    padding: 0px 25px;
                }
        }
        .text{
            color: $lightgrey-font;
            font-size: 18px;
            margin: 20px 0;
            padding-right: 300px;
            font-weight: 400;
        }

    }
.row{
    position: relative;
    padding: 0;
    padding-top: 100px;
    
    .btn{
        width: 120px;
        position: absolute;
        bottom: 25px;
        right: 0;
    }
}
.row-card{
    padding: 0;
    margin-top: 30px;
    padding-bottom: 70px;
}
.card{
    display: inline-block;
    background-color: white;
    padding: 40px 45px;
    margin-bottom: 25px;

        i{
            font-size: 30px;
            color: $green-font;
        }
        h3{
            padding: 15px 0;
        }
        .fa-arrow-right{
            font-size: 25px;
            position: absolute;
            top: 30px;
            right: 35px;
            color: $green-font;
        }
}

}
// Section 3 //
#management{
    .col{
        text-align: center;
        p{
        color: $green-font;
        font-size: 18px;
        margin-bottom: 30px;
        font-weight: 700;
        }
        h2{
            font-size: 56px;
            font-weight: 900;
            margin: 0;
            margin-bottom: 10px;
                span{
                    background-color: $ligthgreen-bg;
                    color: $btn-green-bg;
                    border-radius: 5px;
                    padding: 0px 25px;
                }
        }
        .text{
            text-align: center;
            color: $lightgrey-font;
            font-size: 18px;
            margin: 20px 0;
            font-weight: 400;
            padding: 0 560px;
        }
    }
    .row{
        width: 100%;
        padding: 0;
        padding-top: 90px;
    }
    .row-line{
        position: relative;
        padding-top: 0;
        padding-bottom: 90px;
            .line{
                height: 5px;
                position: absolute;
                top: 105px;
                left: 0;
                right: 0;
                color: $ligthgreen-bg;
                background-color: $ligthgreen-bg;
            }
            .num-card{
                top: -65px;
                left: 100px;
                text-align: center;
                .circle{
                    width: 40px;
                    height: 40px;
                    background-color: $ligthgreen-bg;
                    border-radius: 50%;
                    text-align: center;
                    line-height: 40px;
                    display: inline-block;
                    color: $btn-green-bg;
                }
                h3{
                    padding-bottom: 20px;
                }
                p{
                    color: $lightgrey-font;
                }
            }
    }
    .wrapper{
        width: 90%;
        margin: 0 auto;
        position: relative;
    }
}
//Section4//
#team{
    background-color: $main-dark-bg;
    width: 100%;
}
.col-9{
    color: white;
        p{
            color: $green-font;
            font-size: 18px;
            margin-bottom: 30px;
            font-weight: 700;
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
                font-weight: 400;
        }
}
.row-team{
    padding: 0;
}
.team-card{
    display: flex;
    align-items: center;
    img{
        width: 30%;
        border-radius: 10px;
        display: inline-block;
        margin-right: 30px;
        
    }
    .text{
        display: inline-block;
        margin: 20px 0;
            h3{
                color: white;
            }
            p{
                margin: 20px 0;
                color: $lightgrey-font;
                font-size: 16px;
            }
            i{
                width: 40px;
                height: 40px;
                border-radius: 50%;
                margin:0 5px;
                background-color: $dark-green-bg;
                text-align: center;
                line-height: 40px;
            }
            .fa-brands{
                color: $green-font;
            }
    }
}
.box{
    background-color: $btn-green-bg;
    margin-top: 80px;
    width: 350px;
    border-radius: 5px;
    padding: 20px 35px;
    position: relative;
        h3{
            color: white;
            padding-bottom: 20px;
        }
        p{
            color: $lightgrey-font;
        }
        .cit{
            color: white;
        }
        .fa-quote-right{
            position: absolute;
            font-size: 30px;
            bottom: 30px;
            right: 40px;
            color: $dark-green-bg;
        }
}
//Sezione 5//
.col{
        position: relative;
        p{
        color: $green-font;
        font-size: 18px;
        margin-bottom: 30px;
        font-weight: 700;
        }
        h2{
            font-size: 56px;
            font-weight: 900;
            margin: 0;
            margin-bottom: 10px;
                span{
                    background-color: $ligthgreen-bg;
                    color: $btn-green-bg;
                    border-radius: 5px;
                    padding: 0px 25px;
                }
        }
        .text{
            color: $lightgrey-font;
            font-size: 18px;
            margin: 20px 0;
            padding-right: 300px;
            font-weight: 400;
        }

}
.row{
    position: relative;
    padding: 0;
    padding-top: 100px;
    
    .btn{
        width: 120px;
        position: absolute;
        bottom: 25px;
        right: 0;
    }
}
.img-box{
    border-radius: 10px;
    position: relative;
    overflow: hidden;
    text-align: center;
        img{
            width: 100%;
            object-fit: cover;
            border-radius: 10px;
        }
        .overlay{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.377);
        }
        p{

            position: absolute;
            bottom: 30px;
            left: 0px;
            padding: 0 20px;
            color: white;
            font-size: 30px;
            line-height: 30px;
        }
}
.row-news{
    padding-top: 40px;
    padding-bottom: 90px;
}
</style>