<script setup>
const googleMapsUrl = "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2787.4646861759957!2d14.307869596046263!3d48.743388587722464!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4773663885400329%3A0x64e903a70f46446f!2sVlasta%20Koloniczov%C3%A1!5e0!3m2!1scs!2scz!4v1666619835037!5m2!1scs!2scz"
</script>

<template>
<section class="py-5 px-0 md:px-5">
    <iframe
        class="border-0 w-full max-w-4xl h-[600px] mx-auto rounded-none md:rounded-lg"
        :src="googleMapsUrl"
        allowfullscreen
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
    ></iframe>
</section>
</template>
