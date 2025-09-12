<script setup lang="ts">
    import projects from '@/assets/data/projects.json';
    import Splide from '@splidejs/splide'

    const splide = ref('splide');

	onMounted(() => {
        nextTick(() => {
            const slider =  new Splide(splide.value, {
                perPage: 4,
                perMove: 1,
                arrows: false,
                breakpoints: {
                    1082: {
                        perPage: 3
                    },
                    760: {
                        perPage: 2
                    },
                    510: {
                        perMove: 1
                    }
                }
            })

            slider.on( 'pagination:mounted', function ( data ) {
                // You can add your class to the UL element
                data.list.classList.add('translate-y-12');

                // `items` contains all dot items
                // data.items.forEach( function ( item ) {
                //     item.button.textContent = String( item.page + 1 );
                // } );
            } );
            slider.mount();
        });
    }) ;
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
            <div ref="splide" class="splide w-full max-w-5xl">
                <div class="splide__track">
                    <ul class="splide__list">
                        <li
                            v-for="project in projects"
                            :key="project.id"
                            class="splide__slide flex justify-center"
                        >
                            <ProjectCard :project />
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        
    </div>
</template>