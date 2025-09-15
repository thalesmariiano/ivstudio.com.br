<script setup lang="ts">
    import projects from '@/assets/data/projects.json';

    import emblaCarouselVue from 'embla-carousel-vue';

    const [emblaRef, emblaApi] = emblaCarouselVue({
        loop: false,
        align: 'start'
    });

    onMounted(() => {
        const dotsNode = document.querySelector('.embla__dots') as HTMLElement;
        let dots: HTMLElement[] = []

        nextTick(() => {
            const addDotBtnsAndClickHandlers = () => {
                if(!emblaApi.value) return;

                const addDotBtnsWithClickHandlers = () => {
                    dotsNode.innerHTML = emblaApi.value?.scrollSnapList().map(() => '<button class="embla__dot" type="button"></button>').join('') as string

                    const scrollTo = (index: number) => {
                        emblaApi.value!.scrollTo(index)
                    }

                    dots = Array.from(dotsNode.querySelectorAll('.embla__dot'))

                    dots.forEach((dotNode, index) => {
                        dotNode.addEventListener('click', () => scrollTo(index), false)
                    })
                }
                  

                const toggleDotBtnsActive = () => {
                    const previous = emblaApi.value?.previousScrollSnap()
                    const selected = emblaApi.value?.selectedScrollSnap()
                    // @ts-ignore
                    dots[previous].classList.remove('embla__dot--selected')
                    // @ts-ignore
                    dots[selected].classList.add('embla__dot--selected')
                }

                emblaApi.value
                    .on('init', addDotBtnsWithClickHandlers)
                    .on('reInit', addDotBtnsWithClickHandlers)
                    .on('init', toggleDotBtnsActive)
                    .on('reInit', toggleDotBtnsActive)
                    .on('select', toggleDotBtnsActive)

                return () => {
                    dotsNode.innerHTML = ''
                }
            }

            const removeDotBtnsAndClickHandlers = addDotBtnsAndClickHandlers() as any
            emblaApi.value?.on('destroy', removeDotBtnsAndClickHandlers)
                
        })
    });
</script>

<template>
    <div class="w-full py-16 bg-gradient-to-t from-black from-70%">
        <div class="w-full max-w-4xl flex justify-between items-center px-3 mx-auto mb-10">
            <p class="font-poppins font-medium text-white italic">
                <span class="text-neutral-500">//</span>
                Confira alguns projetos
            </p>
            <a class="flex gap-2 items-center text-white font-poppins font-light italic">
                Veja mais projetos
                <IconsArrowForward width="18" height="18" stroke="#fff" />
            </a>
        </div>

        <div class="w-full flex justify-center items-center">
            <div class="embla w-full max-w-5xl overflow-hidden" ref="emblaRef">
                <div class="embla__container flex">
                    <div v-for="project in projects"
                        :key="project.id"
                        class="embla__slide flex-[0_0_calc(100%/1)] xs:flex-[0_0_calc(100%/2)] md:flex-[0_0_calc(100%/3)] lg:flex-[0_0_calc(100%/4)] min-w-0"
                    >
                        <ProjectCard class="mx-auto" :project />
                    </div>
                </div>

                <div class="embla__controls">
                    <div class="embla__dots"></div>
                </div>
            </div>
        </div>
    </div>
</template>