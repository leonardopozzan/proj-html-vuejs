<template>
    <div class="my-card">
        <div class="logo"><i :class="logo"></i></div>
        <div class="ps-5">
            <div class="title pb-2">{{title}}</div>
            <div class="overview">{{overview}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        data(){
            return{

            }
        },
        props:['logo','title', 'overview']
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
.my-card{
    width: 50%;
    display: flex;
    padding: 0 10rem 5rem 0;
    .logo{
        flex-shrink: 0;
        width: 60px;
        height: 60px;
        line-height: 60px;
        text-align: center;
        border-radius: 50%;
        background-color: $bg-red;
        font-size: 2rem;
        color: $white;
    }
    .title{
        text-transform: uppercase;
        font-weight: bold;
        font-size: 1.6rem;
    }
    .overview{
        font-size: 1.2rem;
    }
}
</style>