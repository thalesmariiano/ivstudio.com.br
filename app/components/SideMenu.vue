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
            
            <LinkButton
                label="Solicitar Orçamento"
                :icon-width="24"
                :icon-height="24"
                :shine-effect="true"
                content-style="rounded-xl pl-4 pr-3 py-1"
            />
        </nav>
    </div>
</template>