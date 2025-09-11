<template>
    <section class="w-full">
        <div class="w-full h-full flex gap-7 flex-col justify-center items-center px-4 pt-36 pb-5">
            <h1 class="font-poppins text-white font-semibold text-[28px] sm:text-[2.7rem] leading-8 sm:leading-12 text-center">
                Sites que Convertem <br>
                e Impulsionam Seu <br>
                Negócio <br>
            </h1>

            <p class="w-full max-w-[550px] font-poppins font-light text-white leading-5 text-center ">
                Criamos sites que fazem seu negócio vender mais.
                Do design à estrategia, tudo é pensado para
                atrair clientes e gerar conversões. Simples, bonito e
                eficiente - extamente como seu site deve ser.
            </p>

            <a class="relative after:content-[''] after:w-full after:h-full after:absolute after:top-0 after:left-0 after:bg-white/40 after:blur-xl flex gap-3 items-center bg-gradient-to-r from-neutral-300 from-75% to-neutral-500 px-6 py-1.5 rounded-xl font-poppins font-semibold text-lg whitespace-nowrap cursor-pointer">
                Solicitar Orçamento
                <IconsArrowForward width="24" height="24" stroke="#000" />
            </a>

            <div class="flex gap-2 items-center">
                <a><IconsGithub width="30" height="30" fill="#fff" /></a>
                <a><IconsBehance width="30" height="30" fill="#fff" /></a>
                <a><IconsInstagram width="30" height="30" fill="#fff" /></a>
                <a><IconsPinterest width="30" height="30" fill="#fff" /></a>
            </div>
        </div>

       <div class="space-y-5 bg-neutral-900/50 py-5 mt-12">
            <ToolsSlider :direction="0.2">
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/html.png" />
                        <span class="font-poppins font-light text-white text-sm">HTML 5</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/css.png" />
                        <span class="font-poppins font-light text-white text-sm">CSS</span>
                    </div>  
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/nitro.png" />
                        <span class="font-poppins font-light text-white text-sm">Nitro</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/js.png" />
                        <span class="font-poppins font-light text-white text-sm">Javascript</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/mysql.png" />
                        <span class="font-poppins font-light text-white text-sm">MySQL</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/nuxt.png" />
                        <span class="font-poppins font-light text-white text-sm">Nuxt.js</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/php.png" />
                        <span class="font-poppins font-light text-white text-sm">PHP</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/tailwind.png" />
                        <span class="font-poppins font-light text-white text-sm">Tailwind CSS</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/vue.png" />
                        <span class="font-poppins font-light text-white text-sm">Vue.js</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/prisma.svg" />
                        <span class="font-poppins font-light text-white text-sm">Prisma</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-2" src="@/assets/images/slide-icons/mongodb.png" />
                        <span class="font-poppins font-light text-white text-sm">MongoDB</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/postgresql.png" />
                        <span class="font-poppins font-light text-white text-sm">PostgreSQl</span>
                    </div>
                </li>
            </ToolsSlider>
            <ToolsSlider :direction="-0.2">
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/coreldraw.png" />
                        <span class="font-poppins font-light text-white text-sm">Coreldraw</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/inkscape.png" />
                        <span class="font-poppins font-light text-white text-sm">Inkscape</span>
                    </div>
                </li>
                <li class="splide__slide">
                    <div class="w-fit flex gap-2 items-center bg-[#1e1e1e] px-4 py-1.5 rounded-xl">
                        <img class="w-5" src="@/assets/images/slide-icons/photoshop.png" />
                        <span class="font-poppins font-light text-white text-sm">Photoshop</span>
                    </div>
                </li>
            </ToolsSlider>
       </div>
    </section>
</template>