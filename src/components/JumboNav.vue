<template>
    <div class="jumbotron">
        <div class="container">
            <div class="nav">
                <div class="logo"><img src="../assets/nexgen-logo.svg" alt=""></div>
                <ul class="links">
                    <li v-for="(link, index) in navbar" :key="index">{{link}}</li>
                </ul>
                <div class="btn">
                    <a href="#">Get in Touch</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import links from '../links.json';
export default {
    name: 'JumboNav',
    data(){
        return{
            navbar: ["Home", "About", "Services", "Process", "Team", "Blog"],
            link: links,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../styles/vars.scss';
.jumbotron{
    width: 100%;
    height: calc(100vh - 50px);
    background-image: url("../assets/bg-6.jpg");
    background-position: center;
    color: $black-font;
}
.nav{
    width: 100%;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: nowrap;

        .logo{
            height: 100%;
            img{
                height: 100%;
                width: 50%;
            }
        }
}
ul{
    list-style: none;
    font-size: 20px;
    margin-bottom: 0;
        li{
            display: inline-block;
            padding: 0 20px;
            text-transform: uppercase;
            cursor: pointer;
        }
}
li:hover{
    background-color: $btn-green-bg;
    border-radius: 10px;
    color: white;
}
.btn{
    background-color: $btn-green-bg;
    width: 160px;
    height: 50px;
    line-height: 0;

        a{
            text-decoration: none;
            color: white;
            line-height: 35px;
            font-size: 20px;
            text-transform: uppercase;
        }
}
</style>