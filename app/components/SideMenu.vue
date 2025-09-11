<template>
    <div class="w-full max-w-96 h-full bg-black ml-auto pt-10">
        <nav class="flex gap-5 flex-col justify-start items-center">
            <ul class="space-y-5">
                <li class="text-center">
                    <NuxtLink to="/" @click="$emit('close')" class="text-xl text-white font-poppins font-light" active-class="font-semibold">
                        Inicío
                    </NuxtLink>
                </li>
                <li class="text-center">
                    <NuxtLink to="/servicos" @click="$emit('close')" class="text-xl text-white font-poppins font-light" active-class="font-semibold">
                        Serviços
                    </NuxtLink>
                </li>
                <li class="text-center">
                    <NuxtLink to="/portfolio" @click="$emit('close')" class="text-xl text-white font-poppins font-light" active-class="font-semibold">
                        Portfólio
                    </NuxtLink>
                </li>
                <li class="text-center">
                    <NuxtLink to="/contato" @click="$emit('close')" class="text-xl text-white font-poppins font-light" active-class="font-semibold">
                        Contato
                    </NuxtLink>
                </li>
            </ul>
            <a
                class="flex gap-2 items-center font-poppins font-medium bg-gradient-to-r from-neutral-300 from-75% to-neutral-500 px-3 py-1 rounded-xl">
                Solicitar Orçamento
                <IconsArrowForward width="24" height="24" stroke="#000" />
            </a>
        </nav>
    </div>
</template>