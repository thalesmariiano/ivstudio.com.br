<script setup lang="ts">
    useSeoMeta({
        title: 'Portfólio | IV Studio - Creative Design'
    });

    import fabetsImg from '~/assets/images/portfolio/fabets.png'
    import blinkyBannerImg from '~/assets/images/portfolio/blinky_banner.png'
    import solaneCleniaImg from '~/assets/images/portfolio/solane-clenia.png'
    import menutapImg from '~/assets/images/portfolio/menutap.png'
    import betzok1Img from '~/assets/images/portfolio/betzok_1.png'
    import betzok4Img from '~/assets/images/portfolio/betzok_4.png'
    import betzok7Img from '~/assets/images/portfolio/betzok_7.png'
    import betzok9Img from '~/assets/images/portfolio/betzok_9.png'
    import adSocialmediaImg from '~/assets/images/portfolio/ad_socialmedia.png'
    import betzok2Img from '~/assets/images/portfolio/betzok_2.png'
    import fluentxImg from '~/assets/images/portfolio/fluentx.png'
    import pereiraKifferImg from '~/assets/images/portfolio/pereira-e-kiffer.png'
    import menutapPostBannerImg from '~/assets/images/portfolio/menutap-post-banner.png'
    import advocaciaImg from '~/assets/images/portfolio/advocacia.png'
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
                <PortfolioItem
                    :src="fabetsImg"
                    name="Fabets"
                    :categories="['Branding', 'Social Media']"
                    wrapper-class="w-full lg:w-[48.4%] h-72 lg:h-full rounded-3xl"
                    img-class="object-center"
                />
            </div>

            <div class="w-full flex flex-col md:flex-row gap-2 xs:gap-5 lg:gap-10 justify-between">
                <PortfolioItem
                    :src="blinkyBannerImg"
                    name="Blinky"
                    :categories="['Banner', 'Design']"
                    wrapper-class="lg:w-[90%] rounded-3xl"
                />

                <PortfolioItem
                    :src="solaneCleniaImg"
                    name="Solane Clênia"
                    :categories="['Identidade Visual', 'Design']"
                    wrapper-class="lg:w-[90%] rounded-3xl"
                />
            </div>

            <div class="w-full lg:h-[600px] flex flex-col lg:flex-row gap-3 xs:gap-5 lg:gap-10 justify-between">
                <PortfolioItem
                    :src="menutapImg"
                    name="MenuTap"
                    :categories="['SaaS', 'Landing Page', 'UI/UX']"
                    wrapper-class="lg:w-[90%] h-[400px] lg:h-full rounded-3xl"
                    img-class="object-top"
                />

                <div class="lg:w-[90%] flex gap-3 xs:gap-5 flex-col items-center rounded-3xl">
                    <div class="w-full h-1/2 flex gap-2 xs:gap-3 justify-between">
                        <PortfolioItem
                            :src="betzok1Img"
                            name="Betzok"
                            :categories="['Social Media', 'Design']"
                            wrapper-class="rounded-xl xs:rounded-3xl"
                        />
                        <PortfolioItem
                            :src="betzok4Img"
                            name="Betzok"
                            :categories="['Social Media', 'Design']"
                            wrapper-class="rounded-xl xs:rounded-3xl"
                        />
                        <PortfolioItem
                            :src="betzok7Img"
                            name="Betzok"
                            :categories="['Social Media', 'Design']"
                            wrapper-class="rounded-xl xs:rounded-3xl"
                        />
                        <PortfolioItem
                            :src="betzok9Img"
                            name="Betzok"
                            :categories="['Social Media', 'Design']"
                            wrapper-class="rounded-xl xs:rounded-3xl"
                        />
                    </div>
                    <PortfolioItem
                        :src="adSocialmediaImg"
                        name="Blinky"
                        :categories="['Ads', 'Social Media']"
                        wrapper-class="w-full h-[55%] rounded-3xl"
                    />
                </div>
            </div>

            <PortfolioItem
                :src="betzok2Img"
                name="Betzok"
                :categories="['Social Media', 'Design']"
                wrapper-class="w-full lg:h-72 rounded-3xl"
                img-class="object-right md:object-center"
            />

            <div class="w-full lg:h-[500px] flex flex-col lg:flex-row gap-2 xs:gap-5 lg:gap-10 justify-between">
                <PortfolioItem
                    :src="fluentxImg"
                    name="FluentX"
                    :categories="['Web Design', 'UI/UX']"
                    wrapper-class="lg:w-[90%] h-96 lg:h-full rounded-3xl"
                    img-class="object-top"
                />

                <PortfolioItem
                    :src="pereiraKifferImg"
                    name="Pereira & Kiffer"
                    :categories="['Branding', 'Identidade Visual']"
                    wrapper-class="lg:w-[90%] h-[400px] lg:h-full rounded-3xl"
                    img-class="object-top"
                />
            </div>

            <PortfolioItem
                :src="menutapPostBannerImg"
                name="MenuTap"
                :categories="['Banner', 'Social Media']"
                wrapper-class="w-full lg:h-72 rounded-3xl"
                img-class="object-right md:object-center"
            />

            <PortfolioItem
                :src="advocaciaImg"
                name="Advocacia"
                :categories="['Landing Page', 'Web Design']"
                wrapper-class="w-full sm:h-[400px] lg:h-[600px] rounded-3xl"
                img-class="lg:object-center"
            />

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