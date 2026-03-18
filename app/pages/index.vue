<script setup lang="ts">
    useSeoMeta({
        title: 'Inicío | IV Studio - Creative Design'
    });
</script>

<template>
    
    <video class="w-full h-screen overflow-x-hidden object-cover absolute top-0 left-0 -z-5" poster="@/assets/images/video-poster.png" autoplay muted loop playsinline webkit-playsinline disablepictureinpicture preload="auto">
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