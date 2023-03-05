<template>
    <div class="container">
        <Hero />
        <AboutSection />
        <AboutSection2 />
        <FaqSection />
        <TransportationSection />
    </div>
</template>

<script>
import Hero from '../components/Hero.vue';
import AboutSection from '../components/AboutSection.vue';
import AboutSection2 from '../components/AboutSection2.vue';
import FaqSection from '../components/FaqSection.vue';
import TransportationSection from '../components/TransportationSection.vue';


export default {
    name: 'MainView',
    components: {
        Hero,
        AboutSection,
        AboutSection2,
        FaqSection,
        TransportationSection,
    }
}
</script>

<style scoped>
.container {
    height: 100%;
    width: 100%;
}
</style>