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
                        <li class="splide__slide w-[140.625px] sm:w-[673px] h-[250px] md:w-[1346px] md:h-[500px]">
                            <img class="w-full h-full object-[70%] sm:object-[0] object-cover" src="@/assets/images/posters/poster1.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] h-[250px] md:w-[281.25px] md:h-[500px]">
                            <img class="w-full h-full object-cover" src="@/assets/images/posters/poster2.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] h-[250px] md:w-[281.25px] md:h-[500px]">
                            <img class="w-full h-full object-cover" src="@/assets/images/posters/poster3.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] h-[250px] md:w-[281.25px] md:h-[500px]">
                            <img class="w-full h-full object-cover" src="@/assets/images/posters/poster4.png" />
                        </li>
                        <li class="splide__slide w-[140.625px] h-[250px] md:w-[281.25px] md:h-[500px]">
                            <img class="w-full h-full object-cover" src="@/assets/images/posters/poster5.webp" />
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>