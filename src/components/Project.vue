<template>
    <section id="project">
        <div class="container">
            <div class="d-flex justify-content-between align-items-center">
                <div class="col-8">
                    <div class="d-flex align-items-center">
                        <div class="line"></div>
                        <div class="sub-title">project</div>
                    </div>
                    <div class="title">our expert trusted consultants help clients</div>
                </div>
                <div class="arrow">
                    <button><i class="fa-solid fa-arrow-left"></i></button>
                    <button><i class="fa-solid fa-arrow-right"></i></button>
                </div>
            </div>
            <div class="row">
                <div class="col-4"><img src="img/carousel-1.jpg" alt=""></div>
                <div class="col-4"><img src="img/carousel-1.jpg" alt=""></div>
                <div class="col-4"><img src="img/carousel-1.jpg" alt=""></div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
section{
    background-color: $bg-blue-dark;
    padding-top: 12rem;
    padding-bottom: 8rem;
    .line{
        width: 50px;
        background-color: $bg-acqua;
        height: 0.2rem;
        margin-right: 1rem;
    }
    .sub-title{
        color: $text-grey;
        text-transform: uppercase;
    }
    .title{
        @include myTitle();
        line-height: 3rem;
        padding: 1rem 0;
    }
    .arrow{
        button{
            width: 50px;
            height: 50px;
            line-height: 50px;
            background-color: $bg-viloet-button;
            color: $white;
            border: 0;
            margin-left: 1rem;
        }
    }
    .img-box{
        width: calc(100% /3);
    }
}
</style>