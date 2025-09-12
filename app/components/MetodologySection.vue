<script setup lang="ts">
    import gsap from 'gsap';
    import { ScrollTrigger } from 'gsap/all';
    
    if (typeof window !== 'undefined') {
        gsap.registerPlugin(ScrollTrigger);
    }
    ScrollTrigger.normalizeScroll();

    const metodology = useTemplateRef('metodology');

    onMounted(() => {
        nextTick(() => {
            const iconContainers = document.querySelectorAll('.icon-container');
            const progressLines = document.querySelectorAll('.progress-line');
            const infos = document.querySelectorAll('.info');

            const tl = gsap.timeline({
                defaults: {duration: 0.4},
                scrollTrigger: {
                    trigger: metodology.value,
                    start: 'top center',
                    end: 'bottom center',
                    toggleActions: "play none none none", 
                }
            })
            .to(progressLines[0]!, {width: '16rem'})
            .to(iconContainers[1]!, {scale: 1, duration: 0.2}).to(iconContainers[1]!.children[0]!, {opacity: 1, duration: 0.1})
            .to(infos[1]!.children[0]!, {opacity: 1, duration: 0.2})
            .to(infos[1]!.children[1]!, {opacity: 1, duration: 0.2})
            .to(progressLines[1]!, {width: '19em'})
            .to(iconContainers[2]!, {scale: 1, duration: 0.2}).to(iconContainers[2]!.children[0]!, {opacity: 1, duration: 0.1})
            .to(infos[2]!.children[0]!, {opacity: 1, duration: 0.2})
            .to(infos[2]!.children[1]!, {opacity: 1, duration: 0.2})
            .to(progressLines[2]!, {width: '11em'})
            .to(iconContainers[3]!, {scale: 1, duration: 0.2}).to(iconContainers[3]!.children[0]!, {opacity: 1, duration: 0.1})
            .to(infos[3]!.children[0]!, {opacity: 1, duration: 0.2})
            .to(infos[3]!.children[1]!, {opacity: 1, duration: 0.2})
            .to(progressLines[3]!, {width: '19em'})
            .to(iconContainers[4]!, {scale: 1, duration: 0.2}).to(iconContainers[4]!.children[0]!, {opacity: 1, duration: 0.1})
            .to(infos[4]!.children[0]!, {opacity: 1, duration: 0.2})
            .to(infos[4]!.children[1]!, {opacity: 1, duration: 0.2})
            .to(progressLines[4]!, {width: '16em'})
            .to(iconContainers[5]!, {scale: 1, duration: 0.2}).to(iconContainers[5]!.children[0]!, {opacity: 1, duration: 0.1})
            .to(infos[5]!.children[0]!, {opacity: 1, duration: 0.2})
            .to(infos[5]!.children[1]!, {opacity: 1, duration: 0.2})
            .to(progressLines[5]!, {width: '16em'});
        });
    });
</script>

<template>
    <section ref="metodology" class="w-full bg-[#f6f2f2] px-10 py-24">
        <h1 class="font-poppins font-semibold italic text-[#201f21] text-left text-lg pl-16 mb-14">// Nossa Metodologia</h1>

        <div class="w-full max-w-[90rem] flex justify-between items-start mx-auto">

            <div class="space-y-10 relative">
                <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                <div class="icon-container relative w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                    <img class="w-5" src="@/assets/images/icons/document-text.svg" />
                </div>
                <div class="info space-y-2">
                    <div>
                        <span class="font-poppins font-light">01.</span>
                        <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Briefing</p>
                    </div>
                    <p class="font-poppins font-light">
                        Imersão ao negócio <br/>
                        Benchmarking <br/>
                        Briefing <br/>
                        Definição de objetivos <br/>
                        Estudo de possibilidades
                    </p>
                </div>
            </div>
            <div class="space-y-10 relative">
                <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                    <img class="opacity-0 w-5.5" src="@/assets/images/icons/git-branch.svg" />
                </div>
                <div class="info space-y-2">
                    <div class="opacity-[0.1]">
                        <span class="font-poppins font-light">02.</span>
                        <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Arquitetura</p>
                    </div>
                    <p class="font-poppins font-light opacity-[0.1]">
                        Sitemap <br/>
                        Midias e tipos de conteúdo <br />
                        Funcionalidades das páginas <br />
                        Estruturação de conteúdo <br />
                        Definição de materiais
                    </p>
                </div>
            </div>
            <div class="space-y-10 relative">
                <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                    <img class="opacity-0 w-5.5" src="@/assets/images/icons/color-palette.svg" />
                </div>
                <div class="info space-y-2">
                    <div class="opacity-[0.1]">
                        <span class="font-poppins font-light">03.</span>
                        <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Design</p>
                    </div>
                    <p class="font-poppins font-light opacity-[0.1]">
                        Wireframe <br />
                        Keyvisual <br />
                        User Interface <br />
                        Protótipo <br />
                        Layout
                    </p>
                </div>
            </div>
            <div class="space-y-10 relative">
                <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                    <img class="opacity-0 w-5.5" src="@/assets/images/icons/code-slash.svg" />
                </div>
                <div class="info space-y-2">
                    <div class="opacity-[0.1]">
                        <span class="font-poppins font-light">04.</span>
                        <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Front-End</p>
                    </div>
                    <p class="font-poppins font-light opacity-[0.1]">
                        Programação e codificação <br/>
                        Estrutura de páginas <br/>
                        Funcionalidades <br />
                        Responsividade
                    </p>
                </div>
            </div>
            <div class="space-y-10 relative">
                <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                    <img class="opacity-0 w-5.5 rotate-90" src="@/assets/images/icons/albums-outline.svg" />
                </div>
                <div class="info space-y-2">
                    <div class="opacity-[0.1]">
                        <span class="font-poppins font-light">05.</span>
                        <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Homologação</p>
                    </div>
                    <p class="font-poppins font-light opacity-[0.1]">
                        Revisão e testes <br />
                        Integrações <br />
                        Validação de conteúdo <br />
                        Otimização SEO <br />
                        Testes de performance
                    </p>
                </div>
            </div>
            <div class="space-y-10 relative">
                <div class="progress-line w-0 h-1 rounded bg-[#201f21] absolute top-5 left-5"></div>

                <div class="icon-container relative scale-[0.3] w-10 h-10 flex justify-center items-center bg-[#201f21] rounded-full">
                    <img class="opacity-0 w-5.5" src="@/assets/images/icons/checkmark-circle.svg" />
                </div>
                <div class="info space-y-2">
                    <div class="opacity-[0.1]">
                        <span class="font-poppins font-light">06.</span>
                        <p class="font-poppins font-semibold italic text-[#201f21] text-lg">Entrega</p>
                    </div>
                    <p class="font-poppins font-light opacity-[0.1]">
                        Hospedagem <br />
                        Validação <br />
                        Publicação <br />
                        Acompanhamento <br />
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>