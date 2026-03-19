<script setup lang="ts">
    import gsap from 'gsap';

    const zapButton = useTemplateRef('zap_button')
    const zapMessage = useTemplateRef('zap_message');

    onMounted(() => {
        nextTick(() => {
            gsap.timeline({repeat: -1, repeatDelay: 15, yoyo: true})
            .to(zapButton.value, {
                borderColor: '#fff',
                delay: 1
            })
            .to(zapMessage.value, {
                x: 8,
                opacity: 1,
                scale: 1,
            });
        });
    });
</script>

<template>
    <div class="fixed right-5 bottom-5 flex items-center">
        <div ref="zap_message" class="flex gap-x-2 items-center scale-0 bg-white px-4 py-1 rounded-l-2xl translate-x-44 opacity-0">
            <div class="w-2 h-2 bg-green-500 shadow-[0_0_10px_rgba(0,255,0)] rounded-full"></div>
            <p class="font-poppins text-black text-sm sm:text-base">Estamos online!</p>
        </div>
        <NuxtLink
            ref="zap_button"
            to="https://api.whatsapp.com/send?phone=558291838543&text=Ol%C3%A1!%20Vim%20pelo%20site%20https://ivstudio.com.br!"
            target="_blank"
            class="w-18 sm:w-20 h-18 sm:h-20 flex justify-center items-center bg-green-500 rounded-full cursor-pointer hover:-translate-y-2 border-2 border-transparent hover:border-white transition-all z-50">
            <IconsWhatsapp width="44" height="44" fill="#fff" />
        </NuxtLink>
    </div>
</template>