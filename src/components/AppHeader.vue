<template>
    <header>
        <div class="infos container">
            <div class="schedule">
                <i class="fa-solid fa-clock"></i><span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
            </div>
            <div class="contacts">
                <i class="fa-solid fa-phone"></i><span>+1 &lpar;305&rpar; 1234-5678</span>
                <i class="fa-solid fa-envelope"></i><span>Hello@example.com</span>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-linkedin-in"></i>
            </div>
        </div>
        <jumbo-nav />
    </header>
</template>

<script>
import JumboNav from './JumboNav.vue';
export default {
    name: 'AppHeader',
    components:{
        JumboNav,
    }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';
header{
    background-color: $dark-blue-bg;
    color: $grey-font;
    font-size: 15px;
}
.infos{
    height: 50px;
    display: flex;
    align-content: center;
    justify-content: space-between;
    align-items: center;
}
.contacts{
    span{
        margin-right: 20px;
    }
    .fa-brands{
        margin: 0 15px;
    }
}
.fa-solid{
    padding-right: 5px;
}
</style>