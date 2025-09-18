<script setup lang="ts">
    import gsap from 'gsap';
    import { ScrollTrigger, MotionPathPlugin } from 'gsap/all';
    
    if (typeof window !== 'undefined') {
        gsap.registerPlugin(ScrollTrigger, MotionPathPlugin);
    }
    ScrollTrigger.normalizeScroll();

    const metodology = useTemplateRef('metodology');

    onMounted(() => {
        nextTick(() => {
            const iconContainers = document.querySelectorAll('.icon-container');
            const progressLines = document.querySelectorAll('.progress-line');
            const infos = document.querySelectorAll('.info');

            let mm = gsap.matchMedia();

            mm.add("(min-width: 1024px)", () => {
                const tl = gsap.timeline({
                    defaults: {duration: 0.4},
                    scrollTrigger: {
                        trigger: metodology.value,
                        start: 'top center',
                        end: 'bottom center',
                        toggleActions: "play none none none", 
                    }
                })
                .to(progressLines[0]!, {width: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[1]!).x + 20})
                .to(iconContainers[1]!, {scale: 1, duration: 0.2}).to(iconContainers[1]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[1]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[1]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {width: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[2]!).x + 20})
                .to(iconContainers[2]!, {scale: 1, duration: 0.2}).to(iconContainers[2]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[2]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[2]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {width: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[3]!).x + 20})
                .to(iconContainers[3]!, {scale: 1, duration: 0.2}).to(iconContainers[3]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[3]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[3]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {width: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[4]!).x + 20})
                .to(iconContainers[4]!, {scale: 1, duration: 0.2}).to(iconContainers[4]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[4]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[4]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {width: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[5]!).x + 20})
                .to(iconContainers[5]!, {scale: 1, duration: 0.2}).to(iconContainers[5]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[5]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[5]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {width: '100%'});
            });

            mm.add("(max-width: 1023px)", () => {
                const tl = gsap.timeline({
                    defaults: {duration: 0.4},
                    scrollTrigger: {
                        trigger: metodology.value,
                        start: 'top center',
                        end: 'bottom center',
                        toggleActions: "play none none none", 
                    }
                })
                .to(progressLines[0]!, {height: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[1]!).y + 20})
                .to(iconContainers[1]!, {scale: 1, duration: 0.2}).to(iconContainers[1]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[1]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[1]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {height: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[2]!).y + 20})
                .to(iconContainers[2]!, {scale: 1, duration: 0.2}).to(iconContainers[2]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[2]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[2]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {height: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[3]!).y + 20})
                .to(iconContainers[3]!, {scale: 1, duration: 0.2}).to(iconContainers[3]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[3]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[3]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {height: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[4]!).y + 20})
                .to(iconContainers[4]!, {scale: 1, duration: 0.2}).to(iconContainers[4]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[4]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[4]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {height: MotionPathPlugin.getRelativePosition(iconContainers[0]!, iconContainers[5]!).y + 20})
                .to(iconContainers[5]!, {scale: 1, duration: 0.2}).to(iconContainers[5]!.children[0]!, {opacity: 1, duration: 0.1})
                .to(infos[5]!.children[0]!, {opacity: 1, duration: 0.2})
                .to(infos[5]!.children[1]!, {opacity: 1, duration: 0.2})
                .to(progressLines[0]!, {height: '100%'});
            });

            

        });
    });
</script>

<template>
    <section ref="metodology" class="w-full bg-[#f6f2f2] px-5 xl:px-10 py-24">
        <div class="w-full max-w-2xl lg:max-w-4xl mx-auto">
            <h1 class="font-poppins font-semibold italic text-[#201f21] text-left text-lg mb-14 pl-5 sm:pl-0">// Nossa Metodologia</h1>
        </div>

        <div class="w-full max-w-[90rem] flex flex-col justify-between items-center lg:items-start mx-auto">

            <div class="relative lg:w-full flex gap-y-12 lg:gap-y-0 flex-col lg:flex-row justify-between mx-auto">
                <div class="absolute left-4.5 lg:left-0 lg:top-4.5 progress-line w-1 h-0 lg:w-0 lg:h-1 rounded bg-[#201f21]"></div>

                <div class="w-fit flex flex-row lg:flex-col gap-10 relative">
                    <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                    <div class="icon-container relative w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                        <img class="w-5" src="@/assets/images/icons/document-text.svg" />
                    </div>
                    <div class="info space-y-2">
                        <div>
                            <span class="font-poppins font-light">01.</span>
                            <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Briefing</p>
                        </div>
                        <p class="font-poppins font-light text-sm lg:text-[12px] xl:text-base">
                            Imersão ao negócio <br/>
                            Benchmarking <br/>
                            Briefing <br/>
                            Definição de objetivos <br/>
                            Estudo de possibilidades
                        </p>
                    </div>
                </div>
                <div class="w-fit flex flex-row lg:flex-col gap-10 relative">
                    <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                    <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                        <img class="opacity-0 w-5.5" src="@/assets/images/icons/git-branch.svg" />
                    </div>
                    <div class="info space-y-2">
                        <div class="opacity-[0.1]">
                            <span class="font-poppins font-light">02.</span>
                            <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Arquitetura</p>
                        </div>
                        <p class="font-poppins font-light text-sm lg:text-[12px] xl:text-base opacity-[0.1]">
                            Sitemap <br/>
                            Midias e tipos de conteúdo <br />
                            Funcionalidades das páginas <br />
                            Estruturação de conteúdo <br />
                            Definição de materiais
                        </p>
                    </div>
                </div>
                <div class="w-fit flex flex-row lg:flex-col gap-10 relative">
                    <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                    <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                        <img class="opacity-0 w-5.5" src="@/assets/images/icons/color-palette.svg" />
                    </div>
                    <div class="info space-y-2">
                        <div class="opacity-[0.1]">
                            <span class="font-poppins font-light">03.</span>
                            <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Design</p>
                        </div>
                        <p class="font-poppins font-light text-sm lg:text-[12px] xl:text-base opacity-[0.1]">
                            Wireframe <br />
                            Keyvisual <br />
                            User Interface <br />
                            Protótipo <br />
                            Layout
                        </p>
                    </div>
                </div>
                <div class="w-fit flex flex-row lg:flex-col gap-10 relative">
                    <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                    <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                        <img class="opacity-0 w-5.5" src="@/assets/images/icons/code-slash.svg" />
                    </div>
                    <div class="info space-y-2">
                        <div class="opacity-[0.1]">
                            <span class="font-poppins font-light">04.</span>
                            <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Front-End</p>
                        </div>
                        <p class="font-poppins font-light text-sm lg:text-[12px] xl:text-base opacity-[0.1]">
                            Programação e codificação <br/>
                            Estrutura de páginas <br/>
                            Funcionalidades <br />
                            Responsividade
                        </p>
                    </div>
                </div>
                <div class="w-fit flex flex-row lg:flex-col gap-10 relative">
                    <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                    <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                        <img class="opacity-0 w-5.5 rotate-90" src="@/assets/images/icons/albums-outline.svg" />
                    </div>
                    <div class="info space-y-2">
                        <div class="opacity-[0.1]">
                            <span class="font-poppins font-light">05.</span>
                            <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Homologação</p>
                        </div>
                        <p class="font-poppins font-light text-sm lg:text-[12px] xl:text-base opacity-[0.1]">
                            Revisão e testes <br />
                            Integrações <br />
                            Validação de conteúdo <br />
                            Otimização SEO <br />
                            Testes de performance
                        </p>
                    </div>
                </div>
                <div class="w-fit flex flex-row lg:flex-col gap-10 relative">
                    <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                    <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                        <img class="opacity-0 w-5.5" src="@/assets/images/icons/checkmark-circle.svg" />
                    </div>
                    <div class="info space-y-2">
                        <div class="opacity-[0.1]">
                            <span class="font-poppins font-light">06.</span>
                            <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Entrega</p>
                        </div>
                        <p class="font-poppins font-light text-sm lg:text-[12px] xl:text-base opacity-[0.1]">
                            Hospedagem <br />
                            Validação <br />
                            Publicação <br />
                            Acompanhamento <br />
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>