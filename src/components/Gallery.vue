<script setup>
import { ref } from "vue"
import useEmitter from "../helpers/useEmitter.js"
import Modal from "./Modal.vue"

import brankaUrl from "../assets/branka.jpg"
import kocourUrl from "../assets/kocour.jpg"
import kunUrl from "../assets/kun.jpg"
import oknoUrl from "../assets/okno.jpg"
import pesAKockaUrl from "../assets/pes-a-kocka.jpg"
import pokoje1Url from "../assets/pokoje-1.jpg"
import pokoje2Url from "../assets/pokoje-2.jpg"
import pokoje3Url from "../assets/pokoje-3.jpg"
import pokoje4Url from "../assets/pokoje-4.jpg"
import pokoje5Url from "../assets/pokoje-5.jpg"
import pokoje6Url from "../assets/pokoje-6.jpg"
import zahonyUrl from "../assets/zahony.jpg"
import zahony2Url from "../assets/zahony-2.jpg"
import terasaUrl from "../assets/terasa.jpg"


const emitter = useEmitter()

const gallery = ref(null)

emitter.on("scrollTo:gallery", _ => {
    gallery.value.scrollIntoView({ behavior: "smooth" })
})

const openModal = e => {
    const src = e.target.src
    const alt = e.target.alt
    emitter.emit("modal:open", { src, alt })
}
</script>

<template>
<Modal />

<section class="min-h-screen">
    <section ref="gallery" class="overflow-hidden text-gray-700">
    <div class="container px-2 md:px-5 py-2 mx-auto lg:pt-24 lg:px-32">
        <p class="mb-8 text-slate-700 text-center">Pro zvětšení klikněte na obrázek</p>

        <div class="flex flex-wrap -m-1 md:-m-2">
        <div class="flex flex-wrap w-full md:w-1/2">
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="oknoUrl">
            </div>
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="kocourUrl">
            </div>
            <div class="w-full p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="kunUrl">
            </div>
        </div>
        <div class="flex flex-wrap w-full md:w-1/2">
            <div class="w-full p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="brankaUrl">
            </div>
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="pesAKockaUrl">
            </div>
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="zahonyUrl">
            </div>
        </div>
        <div class="flex flex-wrap w-full md:w-1/2">
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="pokoje1Url">
            </div>
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="pokoje2Url">
            </div>
            <div class="w-full p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="pokoje3Url">
            </div>
        </div>
        <div class="flex flex-wrap w-full md:w-1/2">
            <div class="w-full p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="pokoje4Url">
            </div>
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="pokoje5Url">
            </div>
            <div class="w-1/2 p-0.5 md:p-2">
            <img @click="openModal" alt="gallery" class="cursor-pointer block object-cover object-center w-full h-full rounded-lg"
                :src="pokoje6Url">
            </div>
        </div>
        </div>
    </div>
    </section>
</section>
</template>
