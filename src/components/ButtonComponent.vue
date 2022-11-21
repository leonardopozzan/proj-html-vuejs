<template>
    <button class="my-btn" :style="{backgroundColor : bgColor,color : textColor}">{{text}}</button>
</template>

<script>
    export default {
        props:['text','textColor','bgColor']
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
.my-btn{
    text-transform: uppercase;
    padding: 0.7rem 3rem;
}
</style>