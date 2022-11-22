<template>
    <section id="about-us">
        <div class="d-flex align-items-center">
            <div class="img-box me-3"><img src="img/business-people-working-together-on-project-and-5FHSKBL.jpg" alt=""></div>
            <div class="ps-5 box">
                <div class="d-flex align-items-center">
                    <div class="line"></div>
                    <div class="sub-title">about us</div>
                </div>
                <div class="title">we make your strategy work</div>
                <div>
                    When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow plants are noticed when I hear the buzz of the little world among the stalks, and grow familiar indescribable forms of the insects and filies, then I fell the presence of the Almighty.
                </div>
            </div>
        </div>
        <div class="info">
            <div class="col-4 pe-5 me-5">we help to deliver the business case</div>
            <div class="col-4 ps-5 ps-5">When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknow</div>
            <ButtonComponent text="get started" bgColor="#F00E2E" class="my-btn"/>
        </div>
    </section>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue';
    export default {
        components: { ButtonComponent }
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
section{
    background-color: $bg-blue-dark;
    .img-box{
        width: 55%;
        height: 600px;
        overflow: hidden;
    }
    .box{
        width: 40%;
        color: $white;
        .line{
            width: 50px;
            background-color: $bg-acqua;
            height: 0.2rem;
            margin-right: 1rem;
        }
        .sub-title{
            text-transform: uppercase;
            color: $white;
        }
        .title{
            @include myTitle(3.5rem);
            line-height: 3.2rem;
            padding: 2rem 0;
        }
    }
    
    .info{
        position: relative;
        background-color: $bg-acqua;
        width: 98%;
        padding: 7rem 0;
        display: flex;
        align-items: center;
        justify-content: center;
        & div:first-child{
            @include myTitle(2.2rem);
            color: black;
        }
        .my-btn{
            position: absolute;
            bottom: 0; right: 0;
            color: $white;
        }
    }
}
</style>