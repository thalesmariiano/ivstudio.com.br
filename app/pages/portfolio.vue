<script setup lang="ts">
    useSeoMeta({
        title: 'Portfólio | IV Studio - Creative Design'
    });
</script>

<template>
    <section class="w-full px-5 py-10 sm:py-14 lg:py-20">

        <div class="w-full max-w-2xl lg:max-w-6xl flex gap-3 xs:gap-5 lg:gap-9 flex-col justify-betweeb mx-auto">

            <div class="w-full lg:h-72 flex flex-col lg:flex-row gap-10 items-center lg:justify-between lg:items-start">
                <div class="w-full max-w-md lg:max-w-[32rem] lg:w-1/2 space-y-5">
                    <h1
                        class="w-52 text-center py-2.5 rounded-3xl font-poppins font-extralight uppercase text-sm text-white tracking-[4px] bg-[rgb(32,32,32)] mx-auto lg:mx-0">
                        Portfólio
                    </h1>
                    <div class="space-y-10">
                        <div class="space-y-3 text-center lg:text-left">
                            <h2 class="font-poppins font-bold text-white text-3xl">Nossos Projetos</h2>
                            <p class="font-poppins font-light text-white">
                                Conheça os projetos que já ajudaram marcas a se destacar no
                                digital. Cada trabalho é pensado para unir estratégia e design,
                                gerando resultados reais
                            </p>
                        </div>

                        <LinkButton
                            label="Vamos criar algo juntos?"
                            :icon-width="24"
                            :icon-height="24"
                            :shine-effect="true"
                            :shine-blur="true"
                            class="w-fit mx-auto lg:mx-0"
                            content-style="rounded-xl px-6 py-1.5 text-lg font-semibold whitespace-nowrap"
                        />
                    </div>
                </div>
                <div class="group w-full lg:w-1/2 h-72 lg:h-full rounded-3xl overflow-hidden">
                    <img class="w-full h-full group-hover:scale-105 transition-all object-cover rounded-3xl" src="@/assets/images/portfolio/fabets.png" />
                </div>
            </div>

            <div class="w-full flex flex-col md:flex-row gap-2 xs:gap-5 lg:gap-10 justify-between">
                <div class="group lg:w-[90%] rounded-3xl overflow-hidden">
                    <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/blinky_banner.png" />
                </div>

                <div class="group lg:w-[90%] rounded-3xl overflow-hidden">
                    <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/solane-clenia.png" />
                </div>  
            </div>

            <div class="w-full lg:h-[600px] flex flex-col lg:flex-row gap-3 xs:gap-5 lg:gap-10 justify-between">
                <div class="group lg:w-[90%] h-[400px] lg:h-full rounded-3xl overflow-hidden">
                    <img class="w-full h-full object-cover object-top group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/menutap.png" />
                </div>

                <div class="lg:w-[90%] flex gap-3 xs:gap-5 flex-col items-center rounded-3xl">
                    <div class="w-full h-1/2 flex gap-2 xs:gap-3 justify-between">
                        <div class="group rounded-xl xs:rounded-3xl overflow-hidden">
                            <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-xl xs:rounded-3xl" src="@/assets/images/portfolio/betzok_1.png" />
                        </div>
                        <div class="group rounded-xl xs:rounded-3xl overflow-hidden">
                            <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-xl xs:rounded-3xl" src="@/assets/images/portfolio/betzok_4.png" />
                        </div>
                        <div class="group rounded-xl xs:rounded-3xl overflow-hidden">
                            <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-xl xs:rounded-3xl" src="@/assets/images/portfolio/betzok_7.png" />
                        </div>
                        <div class="group rounded-xl xs:rounded-3xl overflow-hidden">
                            <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/betzok_9.png" />
                        </div>
                    </div>
                    <div class="group w-full h-[55%] rounded-3xl overflow-hidden">
                        <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/ad_socialmedia.png" />
                    </div>
                </div>
            </div>

            <div class="group w-full lg:h-72 rounded-3xl overflow-hidden">
                <img class="w-full h-full object-cover object-right md:object-center group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/betzok_2.png" />
            </div>

            <div class="w-full lg:h-[500px] flex flex-col lg:flex-row gap-2 xs:gap-5 lg:gap-10 justify-between">
                <div class="group lg:w-[90%] h-96 lg:h-full rounded-3xl overflow-hidden bg-neutral-400">
                    <!-- <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/blinky_banner.png" /> -->
                </div>

                <div class="group lg:w-[90%] h-[400px] lg:h-full rounded-3xl overflow-hidden">
                    <img class="w-full h-full object-cover object-top group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/pereira-e-kiffer.png" />
                </div>
            </div>

            <div class="group w-full h-72 rounded-3xl overflow-hidden bg-neutral-400">
                <!-- <img class="w-full h-full object-cover group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/betzok_2.png" /> -->
            </div>

            <div class="group w-full sm:h-[400px] lg:h-[600px] rounded-3xl overflow-hidden">
                <img class="w-full h-full object-cover lg:object-center group-hover:scale-105 transition-all rounded-3xl" src="@/assets/images/portfolio/advocacia.png" />
            </div>

            <div class="w-full h-62 bg-gradient-to-l from-neutral-300/5 via-transparent via-50% to-neutral-300/5 flex gap-5 flex-col justify-center items-center rounded-3xl p-4">
                <div class="space-y-2 text-center">
                    <h2 class="font-poppins font-semibold text-white text-3xl sm:text-4xl">Gostou do que viu?</h2>
                    <p class="font-poppins font-light text-white text-sm">
                        Cada projeto começa com uma conversa.
                    </p>
                </div>

                <LinkButton 
                    label="Entre em contato" 
                    :icon-width="24" 
                    :icon-height="24" 
                    :shine-effect="true"
                    class="w-fit" 
                    content-style="rounded-xl px-6 py-1 text-lg font-semibold whitespace-nowrap"
                />
            </div>
        </div>
    </section>
</template>