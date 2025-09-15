<script setup lang="ts">
    import Splide from '@splidejs/splide';

    const splide = ref('splide');

	onMounted(() => {
        nextTick(() => {
            const slider =  new Splide(splide.value, {
                type: 'loop',
                perPage: 5,
                perMove: 1,
                arrows: false,
                pagination: false,
                fixedWidth: 'fit',
                breakpoints: {}
            })
            slider.mount();
        });
    }) ;
</script>

<template>
    <section class="w-full">
        <div class="w-full flex justify-center items-center">
            <div ref="splide" class="splide w-full">
                <div class="splide__track">
                    <ul class="splide__list">
                        <li class="splide__slide w-[200px] md:w-fit h-[250px] lg:h-[400px]">
                            <img class="w-full h-full object-cover object-[75%]" src="@/assets/images/posters/poster1.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] lg:w-[250px] lg:h-[400px]">
                            <img class="w-full h-full" src="@/assets/images/posters/poster2.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] lg:w-[250px] lg:h-[400px]">
                            <img class="w-full h-full" src="@/assets/images/posters/poster3.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] lg:w-[250px] lg:h-[400px]">
                            <img class="w-full h-full" src="@/assets/images/posters/poster4.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] lg:w-[250px] lg:h-[400px]">
                            <img class="w-full h-full" src="@/assets/images/posters/poster5.webp" />
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>