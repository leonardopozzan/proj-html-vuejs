<template>
    <section>
        <div class="d-flex align-items-center pb-5 mb-4">
            <div class="title">our consultants can help you</div>
            <div class="line"></div>
        </div>
        <div class="cards">
            <CardDescription  v-for="(el,i) in cardDescription" :key="i" :logo="el.logo" :title="el.title" :overview="el.overview" />
        </div>
    </section>
</template>

<script>
import CardDescription from './CardDescription.vue';
import {cardDescription} from '../data/store'
    export default {
        data(){
            return{
                cardDescription
            }
        },
    components: { CardDescription }
}
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;

section{
    padding: 7rem 0 5rem 20rem;
    .title{
        text-transform: uppercase;
        font-size: 1.5rem;
        font-weight: 600;
    }
    .line{
        flex-grow: 1;
        background-color: $bg-acqua;
        height: 0.2rem;
        margin-left: 1rem;
    }
    .cards{
        display: flex;
        flex-wrap: wrap;
    }
}
</style>