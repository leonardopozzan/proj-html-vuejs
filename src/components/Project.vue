<template>
    <section id="project">
        <div class="my-container">
            <div class="d-flex justify-content-between align-items-center">
                <div class="col-8">
                    <div class="d-flex align-items-center">
                        <div class="line"></div>
                        <div class="sub-title">project</div>
                    </div>
                    <div class="title">our expert trusted consultants help clients</div>
                </div>
                <div class="arrow">
                    <button @click="scrollLeft()"><i class="fa-solid fa-arrow-left"></i></button>
                    <button @click="scrollRight()"><i class="fa-solid fa-arrow-right"></i></button>
                </div>
            </div>
            <div class="carousel-container">
                <div class="carousel" ref="carousel">
                    <ItemCarousel v-for="(el,i) in listPath" :key="i" :url="el" />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import ItemCarousel from './ItemCarousel.vue';

    export default {
    data() {
        return {
            i: 0,
            listPath: ["img/carousel-1.jpg", "img/carousel-2.jpg", "img/carousel-3.jpg", "img/carousel-1.jpg", "img/carousel-2.jpg", "img/carousel-3.jpg"]
        };
    },
    methods: {
        scrollRight() {
            if (this.i < 3) {
                this.i++;
                this.$nextTick(() => {
                    this.$refs.carousel.style.transform = `translateX(calc((-1) * 100% * ${this.i} / 3 )`;
                });
            }
            else {
                this.i = 0;
                this.$nextTick(() => {
                    this.$refs.carousel.style.transform = null;
                });
            }
        },
        scrollLeft() {
            if (this.i > 0) {
                this.i--;
                this.$nextTick(() => {
                    this.$refs.carousel.style.transform = `translateX(calc((-1) * 100% * ${this.i} / 3 )`;
                });
            }
            else {
                this.$nextTick(() => {
                    this.$refs.carousel.style.transform = `translateX(80px)`;
                    setTimeout(() => this.$refs.carousel.style.transform = null, 200);
                });
            }
        }
    },
    components: { ItemCarousel }
}
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
section{
    background-color: $bg-blue-dark;
    padding-top: 12rem;
    padding-bottom: 8rem;
    .carousel-container{
        overflow: hidden;
        margin-left: -1rem;
    }
    .carousel{
        display: flex;
        width: 100%;
        transition: 1s;
    }
    .line{
        width: 50px;
        background-color: $bg-acqua;
        height: 0.2rem;
        margin-right: 1rem;
    }
    .sub-title{
        color: $white;
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
            transition: 0.2s;
            &:hover{
                background-color: $bg-acqua;
            }
        }
    }
}
</style>