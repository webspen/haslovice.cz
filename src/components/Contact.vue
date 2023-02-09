<script setup>
import { ref } from "vue"
import useEmitter from "../helpers/useEmitter"


const emitter = useEmitter()

const contact = ref(null)

emitter.on("scrollTo:contact", _ => {
    contact.value.scrollIntoView({ behavior: "smooth", block: "center" })
})

</script>

<template>
<section ref="contact" class="bg-blue-400 my-10 text-white">
<div class="max-w-7xl mx-auto p-5 my-2 md:my-20">
    <h2 class="text-2xl md:text-4xl font-semibold tracking-wide mb-4 text-center md:text-left">Kontakt</h2>
    <dl class="pl-5 py-4 md:py-10">
        <span class="flex flex-col md:flex-row gap-10">
            <span>
                <dt class="text-xl font-semibold">Adresa</dt>
                <dd class="text-lg text-slate-100">Větřní&nbsp;28, 381&nbsp;01&nbsp;Větřní</dd>
            </span>
            <span>
                <dt class="text-xl font-semibold">Telefon</dt>
                <dd class="text-lg text-slate-100">+420&nbsp;606&nbsp;561&nbsp;954</dd>
            </span>
            <span>
                <dt class="text-xl font-semibold">E-mail</dt>
                <dd class="text-lg text-slate-100">haslovice@haslovice.cz</dd>
            </span>
        </span>
    </dl>
    <div class="flex flex-col md:flex-row gap-4 md:gap-8 max-w-4xl">
        <a
            class="select-none inline-flex gap-2 items-center justify-center w-full h-12 mt-5 text-white bg-black rounded-lg shadow-md hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-teal-200 focus:ring-opacity-75"
            href="tel:+420606561954"
        >
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
            </svg>
            Zavolat
        </a>
        <a
            class="select-none inline-flex gap-2 items-center justify-center w-full h-12 mt-5 text-black bg-white rounded-lg shadow-md hover:bg-gray-200 focus:outline-none focus:ring-2 focus:ring-gray-300 focus:ring-opacity-75"
            href="mailto:haslovice@haslovice.cz"
        >
            <!-- Envelope Icon -->
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
            </svg>
            Napsat e-mail
        </a>
    </div>
    <p class="text-sm md:text-lg text-slate-100 mt-8">*Při zrušení objednaného ubytování vám bude naúčtován 20% storno poplatek z ceny ubytování.</p>
</div>
</section>
</template>
