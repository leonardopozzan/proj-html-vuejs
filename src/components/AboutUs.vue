<template>
    <section id="about-us">
        <div class="d-flex align-items-center">
            <div class="img-box"><img src="img/business-people-working-together-on-project-and-5FHSKBL.jpg" alt=""></div>
            <div class="ps-2">
                <div class="d-flex align-items-center">
                    <div class="line"></div>
                    <div class="sub-title">about us</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
section{
    background-color: $bg-blue-dark;
    .img-box{
        width: 55%;
    }
    .line{
            width: 50px;
            background-color: $bg-acqua;
            height: 0.2rem;
            margin-right: 1rem;
        }
}
</style>