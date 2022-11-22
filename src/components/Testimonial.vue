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
            <CardTestimonials v-for="(el,i) in cardTestimonials" :object="el" />
        </div>
    </section>
</template>

<script>
import CardTestimonials from './CardTestimonials.vue';
import { cardTestimonials } from '../data/store';
    export default {
    data() {
        return {
            cardTestimonials
        }
    },
    components: { CardTestimonials }
}
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
section{
    background-color: $bg-blue-dark;
    padding-bottom: 400px;
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
        width: 95%;
        margin-left: auto;
        background-color: $white;
    }
}
</style>