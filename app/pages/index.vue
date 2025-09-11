<script setup lang="ts">
    useSeoMeta({
        title: 'Inicío | IV Studio - Creative Design'
    });
</script>

<template>
    <div class="bg-[url('@/assets/images/start-bg.png')] bg-position-[7rem_5rem] bg-no-repeat bg-black">
        <InicioSection />
        <ProjectsSlider />
    </div>
    <BannersSection />
    <BeneficiosSection />
    <MetodologySection />
    <FAQSection />
</template>