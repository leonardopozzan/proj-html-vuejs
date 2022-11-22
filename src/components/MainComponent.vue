<template>
    <DescriptionComponent />
    <AboutUs />
    <Project />
    <Testimonial />
    <Blog />
    <Contacts />
</template>

<script>
import AboutUs from './AboutUs.vue';
import Project from './Project.vue';
import Testimonial from './Testimonial.vue';
import DescriptionComponent from './DescriptionComponent.vue';
import Blog from './Blog.vue';
import Contacts from './Contacts.vue';

    export default {
    components: { DescriptionComponent, AboutUs, Project, Testimonial, Blog, Contacts }
}
</script>

<style lang="scss" scoped>

</style>