<script setup>
import useEmitter from "../helpers/useEmitter.js"
import dumUrl from "../assets/dum.jpg"


const emitter = useEmitter()

const scrollToGallery = _ => emitter.emit("scrollTo:gallery")
const scrollToContact = _ => emitter.emit("scrollTo:contact")
</script>

<template>
<section class="min-h-screen">
    <div class="flex flex-col md:flex-row min-h-screen gap-0 md:gap-8 lg:gap-20">
        <img class="grow-0 ml-0 md:ml-5 my-0 md:my-auto rounded-none md:rounded-3xl h-full w-full md:w-1/2" :src="dumUrl" alt="dům" />
        <div class="my-auto w-full md:w-2/3 p-5">
            <h1 class="text-3xl lg:text-6xl tracking-wider mb-2 text-blue-500 font-bold">Statek Hašlovice</h1>
            <p class="max-w-prose text-base md:text-xl">
                Statek Hašlovice se nachází ve vesnici nedaleko Českého Krumlova (asi 15 minut cesty autem). Najdete u nás levné ubytování se snídaní za 600Kč/noc na osobu. Nabízíme ubytování v příjemném prostředí za rozumnou cenu s možností pěších a cyklo výletů do okolní přírody. Je zde také možnost výletů na zámek v Českém Krumlově, hrad Rožmberk, nebo třeba, v letních měsících, návštěva pravidelných varhaních koncertů v klášteře ve Vyšším Brodě. Den můžete zakončit v příjemném, domácím prostředí naší hospůdky.
            </p>
            <button class="mt-6 px-4 py-2 bg-blue-500 text-white rounded-lg" @click="scrollToContact">Kontaktovat</button>
        </div>
    </div>
    <div @click="scrollToGallery" class="hidden md:block absolute py-2 bottom-0 left-0 text-white bg-sky-500 hover:bg-sky-400 w-full">
        <!-- Chevron Down Icon -->
        <svg class="w-10 h-10 mx-auto stroke-2" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
        </svg>
    </div>
</section>
</template>
