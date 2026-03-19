<script setup lang="ts">
    useSeoMeta({
        title: 'Inicío | IV Studio - Creative Design',
        ogTitle: 'Inicío | IV Studio - Creative Design',
        ogDescription: 'Criamos sites que fazem seu negócio vender mais.Do design à estrategia, tudo é pensado para atrair clientes e gerar conversões. Simples, bonito e eficiente - exatamente como seu site deve ser.',
        ogUrl: 'https://ivstudio.com.br',
        ogImage: '/ogthumb.webp',
        ogLocale: 'pt_BR',
        ogType: 'website',
        charset: 'utf-8',
    });
</script>

<template>
    
    <video class="w-full h-screen overflow-x-hidden object-cover absolute top-0 left-0 -z-5" poster="@/assets/images/start-bg.png" autoplay muted loop playsinline webkit-playsinline disablepictureinpicture preload="auto">
        <source src="@/assets/videos/hero-video-4.mp4" type="video/mp4">
        <!-- <source src="@/assets/videos/hero-video.ogg" type="video/ogg"> -->
            Your browser does not support the video tag.
    </video>

    <InicioSection />
    <ProjectsSlider />
    <BannersSection />
    <BeneficiosSection />
    <MetodologySection />
    <FAQSection />
</template>