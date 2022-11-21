<template>
    <DescriptionComponent />
    <AboutUs />
    <Project />
    <Testimonial />
</template>

<script>
import AboutUs from './AboutUs.vue';
import Project from './Project.vue';
import Testimonial from './Testimonial.vue';
import DescriptionComponent from './DescriptionComponent.vue';

    export default {
    components: { DescriptionComponent, AboutUs, Project, Testimonial }
}
</script>

<style lang="scss" scoped>

</style>