<template>
    <footer>
        <section id="footer-top">
            <div class="container">
                <div class="row">
                    <div class="col-3">
                        <div class="logo">
                            <img src="../assets/nexgen-logo-footer.svg" alt="">
                        </div>
                        <div class="text">
                            <p>A Functional HTML Template for corporate &amp; Business.</p>
                            <div class="contacts">
                                <i class="fa-solid fa-phone"></i><span>+1 &lpar;305&rpar; 1234-5678</span><br>
                                <i class="fa-solid fa-envelope"></i><span>Hello@example.com</span><br>
                                <i class="fa-solid fa-location-dot"></i><span>Main Avenue, 987</span>
                            </div>
                        </div>
                        <div class="btn reverse">
                            <a href="#">Get in touch</a>
                        </div>
                    </div>
                    <div class="col-9">
                        <div class="navBox">
                            <h4>About</h4>
                            <ul>
                                <li v-for="(link, index) in footerNav.about" :key="index"><i class="fa-solid fa-angle-right"></i>{{link}}
                                </li>
                            </ul>
                        </div>
                        <div class="navBox">
                            <h4>Services</h4>
                            <ul>
                                <li v-for="(link, index) in footerNav.services" :key="index"><i class="fa-solid fa-angle-right"></i>{{link}}</li>
                            </ul>
                        </div>
                        <div class="navBox">
                            <h4>Support</h4>
                            <ul>
                                <li v-for="(link, index) in footerNav.support" :key="index"><i class="fa-solid fa-angle-right"></i>{{link}}</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section id="footer-bottom">
            <div class="container">
                <div class="bottom">
                    <p>Enjoy the low price. We are tracking any intention of piracy.</p>
                    <p>&#169;2020 NEXGEN is Proudly Powered by <span>Codings</span>.</p>
                </div>
            </div>
        </section>
    </footer>
</template>

<script>
import link from '../links.json';
export default {
    name: 'AppFooter',
    data(){
        return{
            footerNav: link,
        }
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';
#footer-top{
   background-color: $main-dark-bg;
   color: $lightgrey-font;
   .reverse{
       a{
            color: white;
       }
   }
    .row{
        padding: 140px 0;
    }
    span{
        display: inline-block;
    }
    .logo{
        height: 50px;
        margin: 20px 0;
        img{
            height: 100%;
            object-fit: cover;
            
        }
    }
    .text{
        font-size: 20px;
        p{
            padding-bottom: 20px;
        }
        .contacts{
            padding-bottom: 40px;
            i{
                padding-right: 15px;
            }
        }
    }
    .col-9{
        display: flex;
        align-items: stretch;
        justify-content: space-evenly;
        gap: 40px;
    }
    .navBox{
        display: inline-block;
        width: 100%;
        padding: 30px 20px;
        background-color: $footer-grey-bg;
        border-radius: 10px;
            h4{
                padding-left: 20px;
                color: white;
                font-weight: 700;
            }
            ul{

                list-style-type: none;
                padding: 10px 20px;
                li{
                    cursor: pointer;
                    i{
                        padding: 8px 0;
                        padding-right: 20px;
                        font-size: 22px;
                    }
                }
            }
    }
}
#footer-bottom{
    background-color: $footer-black-bg;
    color: $lightgrey-font;
    .bottom{
        display: flex;
        justify-content: space-between;
        align-items: center;
        align-content: center;
        padding: 30px 0;
        p{
            margin: 0;
            span{
                color: $btn-green-bg;
                cursor: pointer;
            }
        }
    }
}
</style>