<script setup>
import Hero from "./components/Hero.vue"
import Contact from "./components/Contact.vue"
import Map from "./components/Map.vue"
import Gallery from "./components/Gallery.vue"
import Footer from "./components/Footer.vue"
</script>

<template>
<div>
    <Hero />
    <!-- Switch Gallery and Contact on smaller screens -->
    <span class="flex flex-col-reverse md:flex-col">
        <Gallery />
        <Contact />
    </span>
    <Map />
    <Footer />
</div>
</template>
