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

            <div class="consulting">
                <p>Fusions &amp; acquisition</p>
                <h1>Insurance Consulting</h1>
                <input type="text" placeholder="Name">
                <input type="text" placeholder="Email">
                <input type="text" placeholder="Phone">
                <select name="info" id="info">
                    <option selected value="More Info">More Info</option>
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

        .logo{
            height: 100%;
            img{
                height: 100%;
                width: 45%;
            }
        }
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