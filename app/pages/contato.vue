<script setup lang="ts">
    useSeoMeta({
        title: 'Contato | IV Studio - Creative Design'
    });
</script>

<template>
    <section class="w-full px-5 py-10 sm:py-14 lg:py-20">
        <div class="w-full max-w-2xl lg:max-w-6xl mx-auto space-y-10">
            <div class="w-full space-y-5 text-center">
                <h1
                    class="w-52 text-center py-2.5 rounded-3xl font-poppins font-extralight uppercase text-sm text-white tracking-[4px] bg-[rgb(32,32,32)] mx-auto">
                    Contato
                </h1>

                <div class="space-y-3">
                    <h2 class="font-poppins font-bold text-white text-3xl">Vamos criar algo juntos?</h2>
                    <p class="font-poppins font-light text-white max-w-2xl mx-auto">
                        Preencha o formulário abaixo e me conte o que você precisa. Em poucos passos você envia as informações
                        essenciais para eu retornar com orientações, prazo e orçamento.
                    </p>
                </div>
            </div>

            <ContactFormStepper />
        </div>
    </section>
</template>