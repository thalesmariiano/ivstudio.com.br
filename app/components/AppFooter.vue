<template>
    <footer class="w-full bg-[#0a0a0a] p-10">
        <div class="w-full max-w-5xl flex justify-between items-center mx-auto">
            <div class="w-full lg:w-fit flex gap-3 flex-row lg:flex-col justify-between lg:justify-start items-center lg:items-start">
                <img class="w-28 lg:w-34" src="@/assets/images/ivstudio-logo.png" />
                <div class="flex flex-col lg:flex-row gap-x-2 items-start lg:items-center">
                    <p class="font-poppins font-light text-white text-xs">&copy 2025 IV Studio. </p>
                    <p class="font-poppins font-light text-white text-xs">Todos os direitos reservados.</p>
                </div>
            </div>
            <div class="space-y-3 hidden lg:block">
                <p class="font-poppins font-semibold italic text-white">Navegue:</p>
                <nav class="flex gap-10 items-center">
                    <ul class="flex gap-10 items-center">
                        <li>
                            <NuxtLink
                                to="/"
                                active-class="font-semibold"
                                class="text-white font-poppins font-light text-sm"
                            >
                                Inicío
                            </NuxtLink>
                        </li>
                        <li>
                            <NuxtLink
                                to="/servicos"
                                active-class="font-semibold"
                                class="text-white font-poppins font-light text-sm"
                            >
                                Serviços
                            </NuxtLink>
                        </li>
                        <li>
                            <NuxtLink
                                to="/portfolio"
                                active-class="font-semibold"
                                class="text-white font-poppins font-light text-sm"
                            >
                                Portfólio
                            </NuxtLink>
                        </li>
                        <li>
                            <NuxtLink
                                to="/contato"
                                active-class="font-semibold"
                                class="text-white font-poppins font-light text-sm"
                            >
                                Contato
                            </NuxtLink>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </footer>
</template>