<template>
    <div class="container">
        <Hero />
        <AboutSection />
        <MapSection />
        <TransportationSection />
    </div>
</template>

<script>
import Hero from '../components/Hero.vue';
import AboutSection from '../components/AboutSection.vue';
import MapSection from '../components/MapSection.vue';
import TransportationSection from '../components/TransportationSection.vue';


export default {
    name: 'MainView',
    components: {
        Hero,
        AboutSection,
        MapSection,
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