<script setup lang="ts">
    const { accordionId } = defineProps(['accordionId']);
</script>

<template>
    <div class="accordion group">
        <div class="w-full flex flex-col justify-between items-center">
            <input class="hidden" :id="accordionId" type="radio" name="faq-accordion" />
            <label :for="accordionId" class="accordion-title font-poppins">
                <slot name="question" />
                <img class="w-4 h-4 transition-all group-has-[:checked]:rotate-180" src="@/assets/images/icons/caret-down.svg" />
            </label>

            <div class="accordion-content">
                <p class="font-poppins font-light text-neutral-300 text-sm pb-5">
                    <slot name="answer" />
                </p>
            </div>
        </div> 
    </div>
</template>

<style scoped>
    @reference 'tailwindcss';

    .accordion {
        @apply w-full max-w-lg sm:max-w-2xl relative border-b border-white/30 px-0 sm:px-5 hover:bg-white/20 transition-all
    }
    .accordion-title {
        @apply w-full p-3 cursor-pointer flex justify-between items-center text-sm sm:text-base font-light italic text-white
    }

    .accordion-content {
        @apply w-full px-5 transition-all duration-500 overflow-hidden max-h-0 group-has-[:checked]:max-h-96
    }

    /* .accordion::after {
        content: url(@/assets/images/icons/caret-down.svg);
        width: 16px;
        height: 16px;
        position: absolute;
        right: 25px;
        top: 20px;
        transition: all 500ms
    }

    .accordion:has(:checked)::after {
        rotate: 180deg
    } */
</style>