<template>
    <div @mouseleave="show=false" class="my-card">
        <div class="overlay" @mouseover="show=true" :class="{'bg-red' : show}"></div>
        <img :src="url" alt="" :class="{'scale' : show}">
        <Transition name="slide-left">
            <div class="plus" v-show="show"><div>+</div></div>
        </Transition>
        <Transition name="slide-up">
            <div class="info" v-show="show">
                <div>Purinky Products</div>
                <div>uncategorized</div>
            </div>
        </Transition>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                show : false
            }
        },
        props:['url']
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
.my-card{
    width: calc((100% - 3rem) / 3);
    margin-left: 1rem;
    flex-shrink: 0;
    overflow: hidden;
    position: relative;
}
img{
    transition: 1s;
}
.scale{
    transform: scale(1.1) !important;
}
.bg-red{
    background-color: #f00e2e;
}
.overlay{
    position: absolute;
    top: 0; bottom: 0; right: 0; left: 0;
    z-index: 50;
    transition: 1s;
    mix-blend-mode: darken;
}
.plus{
    position: absolute;
    z-index: 200;
    background-color: $bg-viloet-button;
    right: 15px; bottom: 15px;
    width: 60px;
    height: 60px;
    border: 2px solid black;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2.5rem;
    color: $white;
    transition: 0.25s;
    div{
        transition: 0.25s;
    }
    &:hover div{
        transform-origin: center center;
        transform: rotate(180deg);
    }
    &:hover{
        background-color: $bg-acqua;
    }
}
.info{
    color: $white;
    position: absolute;
    bottom: 15px; left: 15px;
    z-index: 50;
    & div:first-child{
        font-size: 1.4rem;
        font-weight: bold;
    }
    & div:last-child{
        font-size: 1.1rem;
        color: $text-light-grey;
    }
}
.slide-left-enter-active {
        transition: all 1s ease-out;
    }

    .slide-left-leave-active {
        transition: all 1s cubic-bezier(1, 0.5, 0.8, 1);
    }

    .slide-left-enter-from{
        transform: translateX(-150px);
        opacity: 0;
    }
    .slide-left-leave-to {
        transform: translateX(50px);
        opacity: 0;
    }
    .slide-up-enter-active {
        transition: all 1s ease-out;
    }

    .slide-up-leave-active {
        transition: all 1s cubic-bezier(1, 0.5, 0.8, 1);
    }

    .slide-up-enter-from,
    .slide-up-leave-to {
        transform: translateY(50px);
        opacity: 0;
    }
</style>