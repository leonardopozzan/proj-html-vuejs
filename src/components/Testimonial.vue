<template>
    <section>
        <div class="container">
            <div class="d-flex align-items-center justify-content-center">
                <div class="sub-title flex-grow-1">testimonials</div>
                <div class="line"></div>
            </div>
            <div class="title">what's the costumer say about our work</div>
        </div>
        <div class="cards">
            <div class="my-card" @mouseover="styleBg">
                <div>
                    When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when I hear the buzz of the little
                </div>
                <div class="name">
                    Vera Duncan
                </div>
                <div>
                    Amazon Inc.
                </div>
            </div>
            <div class="my-card">
                <div>
                    When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when I hear the buzz of the little
                </div>
                <div class="name">
                    Vera Duncan
                </div>
                <div>
                    Amazon Inc.
                </div>
            </div>
            <div class="my-card">
                <div>
                    When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed by when I hear the buzz of the little
                </div>
                <div class="name">
                    Vera Duncan
                </div>
                <div>
                    Amazon Inc.
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        data(){
            return{

            }
        },
        computed:{
            styleBg(){
                return {'bg-img' : 'img/avatar-1.jpg'}
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
section{
    background-color: $bg-blue-dark;
    .line{
        width: 50px;
        background-color: $bg-acqua;
        height: 0.2rem;
        margin-left: 1rem;
    }
    .sub-title{
        color: $text-grey;
        text-transform: uppercase;
        text-align: center;
    }
    .title{
        @include myTitle();
        line-height: 3rem;
        padding: 1rem 0;
        text-align: right;
        width: 60%;
        margin-left: auto;
    }
    .cards{
        display: flex;
        width: 90%;
        margin-left: auto;
        background-color: $white;
        padding: 2.5rem;
        .my-card{
            width: calc(100% / 3);
            background-color: $white-card;
            margin: 0 6rem 0 1rem;
            padding-right: 1rem;
            display: flex;
            flex-direction: column;
            & div:first-child{
                flex-grow: 1;
                padding-bottom: 2rem;
            }
            .name{
                font-size: 1.4rem;
                font-weight: bold;
            }
        }
    }
}
</style>