<template>
    <section class="position-relative">
        <div class="img-box"><img src="img/business-people-working-together-on-project-and-B3MZ4TX.jpg" alt=""></div>
        <div class="box">
            <div class="title">let's talk about work</div>
            <div class="sub-title">A wonderful serenity has taken possession Far far away, behind the word mountains.</div>
            <ButtonComponent text="get started" bgColor="#1F1E38" textColor="#FFF" bgColorHover="#ffc318" bool="true" />
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
    .box{
        width: 40%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        text-align: center;
        .title{
            @include myTitle();
        }
        .sub-title{
            font-size: 1.2rem;
            color: $white-op;
            padding: 1rem 2rem;
        }
    }
}
</style>