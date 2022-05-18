<template>
    <div class="jumbotron">
        <div class="container">
            <div class="nav">
                <div class="logo"><img src="../assets/nexgen-logo.svg" alt=""></div>
                <ul class="links">
                    <li @click="drop(index)"  v-for="(link, index) in navbar" :key="index" :id="link">{{link}}</li>
                </ul>
                <div @mouseleave="dropleave" :class="drop1 ? 'show' : ''" class="drops abouts">
                    <p v-for="(drop, index) in link.about" :key="index">{{drop}}</p>
                </div>
                <div @mouseleave="dropleave" :class="drop2 ? 'show' : ''" class="drops service">
                    <p v-for="(drop, index) in link.services" :key="index">{{drop}}</p>
                </div>
                <div class="btn">
                    <a href="#">Get in Touch</a>
                </div>
            </div>

            <div class="consulting">
                <p>Fusions &amp; acquisition</p>
                <h1>Insurance Consulting</h1>
                <input type="text" placeholder="Name">
                <input type="text" placeholder="Email">
                <input type="text" placeholder="Phone">
                <select name="info" id="info">
                    <option selected disabled value="---">---</option>
                    <option value="Sales">Sales and Purchasing</option>
                    <option value="Financial">Financial and Accounts</option>
                    <option value="Human">Human Resource</option>
                    <option value="Another">Another subject</option>
                </select>
                <div class="btn">
                    <a href="#">Get in Touch</a>
                </div>
                <div class="btn reverse">
                    <a href="#">Read More</a>
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
            drop1: false,
            drop2: false,
        }
    },
    methods: {
        drop(index){
            let drop1 = this.drop1;
            let drop2 = this.drop2;
            if(drop1 === false){
                if(index === 1){
                this.drop1 = true;
                this.drop2 = false;
                }
            }else{
                if(index === 1){
                this.drop1 = false;
                this.drop2 = false;
                }
            }
            if(drop2 === false){
                if(index === 2){
                this.drop2 = true;
                this.drop1 = false;
                }
            }else{
                if(index === 2){
                this.drop2 = false;
                this.drop1 = false;
                }
            }

        },
        dropleave(){
            this.drop1 = false;
            this.drop2 = false;
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

        .container{
            height: 100%;
            position: relative;
        }
}
.nav{
    width: 100%;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: nowrap;
    position: relative;

        .logo{
            height: 100%;
            img{
                height: 100%;
                width: 45%;
            }
        }
        .drops{
            width: 135px;
            position: absolute;
            top: 64px;
            background-color: white;
            border-radius: 10px;
            text-align: center;
            border: 1px solid $green-font;
            display: none;
            transition: all 0.5s;
                p{
                    margin-bottom: 0;
                    cursor: pointer;
                    padding: 10px 0;
                }
                p:hover{
                    background-color: #b4b4b4;
                }

        }
        .abouts{
            left: 407px;
        }
        .service{
            left: 527px;
        }
}
.show{
    display: block!important;
    z-index: 10000;
    animation: fade 0.8s forwards;
}
@keyframes fade {
    0%{opacity: 0}
    100%{opacity: 1}
}

ul{
    list-style: none;
    font-size: 18px;
    margin-bottom: 0;
        li{
            display: inline-block;
            padding: 0 20px;
            text-transform: uppercase;
            cursor: pointer;
        }
        #About::after{
            font: var(--fa-font-solid);
            content: "\f107";
        }
        #Services::after{
            font: var(--fa-font-solid);
            content: "\f107";
        }
}

li:hover{
    background-color: $btn-green-bg;
    border-radius: 10px;
    color: white;
}

.consulting{
    width: 55%;
    position: absolute;
    top: 50%;
    left: 54%;
    transform: translate(0%, -50%);
        p{
            font-size: 20px;
            color: $green-font;
            margin: 0;
            font-weight: 700;
        }
        h1{
            font-size: 85px;
            font-weight: 900;
            margin-bottom: 20px;
        }
        input{
            width: 250px;
            height: 50px;
            margin: 10px 5px;
            background-color: $input-bg;
            border: 0;
            border-radius: 5px;
            padding: 0 15px;
            font-size: 20px;
        }
        select{
            width: 250px;
            height: 50px;
            margin: 10px 5px;
            background-color: $input-bg;
            border: 0;
            border-radius: 5px;
            padding: 0 15px;
            font-size: 20px;
            color: #7B7575;
        }
        .btn{
            margin: 10px 10px;
        }
        .reverse{
            background-color: transparent;
            border: 1px solid $btn-green-bg;
                a{
                    color: $btn-green-bg;
                }
        }
}
</style>