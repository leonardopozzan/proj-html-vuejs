<template>
    <section>
        <div class="d-flex align-items-center">
            <div class="line"></div>
            <div class="sub-title">testimonials</div>
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
    .line{
        width: 50px;
        background-color: $bg-acqua;
        height: 0.2rem;
        margin-right: 1rem;
    }
    .sub-title{
        color: $text-grey;
        text-transform: uppercase;
    }
}
</style>