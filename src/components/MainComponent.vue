<template>
    <DescriptionComponent />
    <AboutUs />
    <Project />
    <Testimonial />
    <Blog />
</template>

<script>
import AboutUs from './AboutUs.vue';
import Project from './Project.vue';
import Testimonial from './Testimonial.vue';
import DescriptionComponent from './DescriptionComponent.vue';
import Blog from './Blog.vue';

    export default {
    components: { DescriptionComponent, AboutUs, Project, Testimonial, Blog }
}
</script>

<style lang="scss" scoped>

</style>