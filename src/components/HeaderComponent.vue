<template>
    <header>
        <div class="container text-uppercase">
            <nav class="d-flex align-items-center justify-content-between">
                <div class="img-box"><img src="img/logotype.png" alt="logo"></div>
                <ul class="m-0 d-flex">
                    <li v-for="(el,i) in navbar" :key="i" class="px-3 py-4"><a href="el.url">{{el.title}}</a></li>
                </ul>
            </nav>
            <div class="jumbo">
                <div class="d-flex align-items-center">
                    <div class="line"></div>
                    <div class="sub-title">always the best way you need it</div>
                </div>
                <div class="title">the best business consulting</div>
                <div>
                    <ButtonComponent text="read more" bgColor="#39FFBF"/>
                    <i class="fa-solid fa-play play"></i>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
import {navbar} from '../data/store';
import ButtonComponent from './ButtonComponent.vue';
    export default {
    data() {
        return {
            navbar
        };
    },
    components: { ButtonComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
header{
    background-image: url('img/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg');
    background-size: contain;
    background-repeat: no-repeat;
    background-position: right;
    background-color: $bg-blue-dark;

    nav{
        .img-box{
            width: 100px;
        }
        ul{
            li{
                border-top: 2px solid transparent;
                a{
                    color: $white;
                }
            }
        }
    }
    .jumbo{
        width: 40%;
        padding: 12rem 0;
        .sub-title{
            color: $text-grey;
        }
        .line{
            width: 50px;
            background-color: $bg-acqua;
            height: 0.2rem;
            margin-right: 1rem;
        }
        .title{
            padding: 2rem 0;
            color: $white;
            font-size: 4.5rem;
            font-weight: bold;
            line-height: 4rem;
        }
        
        .play{
            color: $bg-acqua-button;
            width: 40px;
            height: 40px;
            text-align: center;
            line-height: 40px;
            border: 1px solid $white;
            border-radius: 50%;
            margin-left: 1.5rem;
        }
    }
}
</style>