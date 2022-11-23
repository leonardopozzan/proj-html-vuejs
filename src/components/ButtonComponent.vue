<template>
    <button class="my-btn" :style="{backgroundColor : bgColor,color : textColor}" @mouseover="show = true" @mouseleave="show = false">
    <span :class="{'color-white' : show, 'color-violet' : bool && show}">{{text}}</span>
    <div class="square" :class="{'scale' : show}" :style="{backgroundColor : bgColorHover}"></div>
    </button>
</template>

<script>
    export default {
        data(){
            return{
                show : false
            }
        },
        props:['text','textColor','bgColor','bgColorHover','bool']
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
.my-btn{
    text-transform: uppercase;
    width: 270px;
    height: 70px;
    font-size: 1.3rem;
    border: 0;
    position: relative;
    span{
        position: relative;
        z-index: 100;
    }
    .square{
        position: absolute;
        top: 50%; left: 50%;
        width: 0;
        height: 0;
        transform: translate(-50%,-50%);
        transition: 1s;
    }
    .scale{
        width: 271px;
        height: 71px;
    }
    .color-white{
        color: $white;
    }
    .color-violet{
        color: $bg-viloet-button;
    }
}
</style>