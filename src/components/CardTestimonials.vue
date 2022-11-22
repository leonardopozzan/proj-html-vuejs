<template>
    <div class="my-card" @mouseover="show=true" @mouseleave="show=false">
        <div class="inner-card" :class="{'text-white' : show}">
                <div>
                    {{object.overview}}
                </div>
                <div class="name">
                    {{object.name}}
                </div>
                <div>
                    {{object.firm}}
                </div>
            </div>
        <div class="img-box" :class="{'opacity-100' : show}" ><img :src="object.img" alt=""></div>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                show: false
            }
        },
        props: ['object']
    }
</script>

<style lang="scss" scoped>

.my-card{
    width: calc(100% / 3);
    position: relative;
    height: 390px;
    overflow: hidden;
    
    .img-box{
        opacity: 0;
        transition: opacity 0.2s;
    }
    .inner-card{
        position: absolute;
        top: 0; left: 0;
        z-index: 500;
        margin: 3rem;
        display: flex;
        flex-direction: column;
        height: calc(100% - 6rem);
        font-size: 1.1rem;
        transition: color 0.2s;
        & div:first-child{
        flex-grow: 1;
        padding-bottom: 2rem;
        }
        .name{
            font-size: 1.6rem;
            font-weight: bold;
        }
    }
}
</style>