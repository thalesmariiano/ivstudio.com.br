<script setup lang="ts">
    import services from "@/assets/data/services.json";

    useSeoMeta({
        title: 'Serviços | IV Studio - Creative Design'
    });
</script>

<template>
    <section class="w-full px-5 py-20">
        <div class="w-full max-w-7xl flex flex-col lg:flex-row gap-10 lg:gap-5 justify-between mx-auto">
            <div class="w-full max-w-xl space-y-5 mx-auto lg:mx-0">
                <h1 class="w-72 text-center py-2.5 rounded-3xl font-poppins font-extralight uppercase text-sm text-white tracking-[4px] bg-[rgb(32,32,32)] mx-auto lg:mx-0">Nossos serviços</h1>
                <div class="space-y-10">
                    <div class="space-y-3 text-center lg:text-left">
                        <h2 class="font-poppins font-bold text-white text-3xl">Eleve seu posicionamento</h2>
                        <p class="font-poppins font-light text-white">
                            Design que conecta sua marca às pessoas certas. Criamos sites,
                            landing pages, posts, anúncios e materiais digitais que chamam
                            atenção, engajam e transformam visitantes em resultados.
                        </p>
                    </div>

                    <LinkButton
                        label="Entrar em contato"
                        :icon-width="24"
                        :icon-height="24"
                        :shine-effect="true"
                        :shine-blur="true"
                        class="w-72 mx-auto lg:mx-0"
                        content-style="rounded-xl px-6 py-1.5 text-lg font-semibold whitespace-nowrap"
                    />
                </div>

                <div class="hidden w-full max-w-[34rem] h-[62rem] lg:grid gap-x-3 gap-y-7 grid-cols-4 grid-rows-7 mt-16">
                    <div class="col-start-1 col-end-5 row-start-1 row-end-4 rounded-3xl">
                        <img class="w-full h-full object-cover m-0 p-0 rounded-3xl border-none outline-none" src="@/assets/images/portfolio/blinky_banner.png"/>
                    </div>
                    <div class="col-start-1 col-end-5 row-start-4 row-end-6">
                        <img class="w-full h-full object-cover m-0 p-0 rounded-3xl border-none outline-none" src="@/assets/images/portfolio/fabets.png"/>
                    </div>
                    <div class="row-start-6 row-end-8 rounded-3xl">
                        <img class="w-full h-full object-cover m-0 p-0 rounded-3xl border-none outline-none" src="@/assets/images/portfolio/betzok_1.png"/>
                    </div>
                    <div class="row-start-6 row-end-8 rounded-3xl">
                        <img class="w-full h-full object-cover m-0 p-0 rounded-3xl border-none outline-none" src="@/assets/images/portfolio/betzok_4.png"/>
                    </div>
                    <div class="row-start-6 row-end-8 rounded-3xl">
                        <img class="w-full h-full object-cover m-0 p-0 rounded-3xl border-none outline-none" src="@/assets/images/portfolio/betzok_7.png"/>
                    </div>
                    <div class="row-start-6 row-end-8 rounded-3xl">
                        <img class="w-full h-full object-cover m-0 p-0 rounded-3xl border-none outline-none" src="@/assets/images/portfolio/betzok_9.png"/>
                    </div>
                </div>
            </div>

            <div class="w-full max-w-2xl bg-[#141414]/50 rounded-[4rem] px-10 sm:px-14 py-3 sm:py-6 flex flex-col mx-auto lg:mx-0">
                <div class="space-y-3 border-b border-white/30 pb-7 mt-7 last:border-none" v-for="service in services" :key="service.id">   
                    <div class="flex gap-x-5 items-center">
                        <p class="font-poppins font-semibold text-2xl text-white">{{ service.title }}</p>
                        <NuxtLink>
                            <IconsChevronForwardCircleOutline width="20" height="20" stroke="#505050" />
                        </NuxtLink>
                    </div>
                    <p class="font-poppins text-white font-light text-[.95rem] leading-5.5">{{ service.description }}</p>
                </div>
            </div>
        </div>
    </section>
</template>