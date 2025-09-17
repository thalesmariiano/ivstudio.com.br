<script setup lang="ts">
    import type { RouteLocationAsPathGeneric, RouteLocationAsRelativeGeneric } from 'vue-router';

    const props = defineProps<{
        to?: string | RouteLocationAsRelativeGeneric | RouteLocationAsPathGeneric | undefined,
        target?: "_blank" | "_parent" | "_self" | "_top" | (string & {}) | null | undefined,
        contentStyle?: string,
        label: string,
        iconWidth: number,
        iconHeight: number,
        shineEffect?: boolean,
        shineBlur?: boolean
    }>();

    const elContent =  useTemplateRef('el-content')

    const showShine = props.shineEffect ? 'shine-effect' : '';
    const showBlur = props.shineBlur ? 'shine-blur' : '';
</script>

<template>
    <div>
        <NuxtLink
            @touchstart="() => elContent?.classList.add('shine-effect', 'shine-effect-mobile')"
            @touchend="() => elContent?.classList.remove('shine-effect', 'shine-effect-mobile')"
            :to="props.to"
            :target="props.target"
            :class="'group ' + showBlur"
        >
            <div ref="el-content" :class="'default-style  ' + showShine + ' ' + props.contentStyle">
                {{ props.label }}
                <IconsArrowForward :width="props.iconWidth" :height="props.iconHeight" stroke="#000" />
            </div>
        </NuxtLink>
    </div>
</template>

<style scoped>
    @reference '@/assets/css/tailwind.css';

    .default-style {
        @apply flex gap-x-2 justify-center items-center cursor-pointer text-black font-poppins font-medium bg-gradient-to-r from-neutral-300 from-75% to-neutral-500
    }

    .shine-blur {
        @apply relative after:content-[''] after:w-full after:h-full after:absolute after:top-0 after:left-0 after:bg-white/40 after:blur-xl cursor-pointer
    }

    .shine-effect {
        @apply relative overflow-hidden group-hover:before:animate-[shine-reflex_1.2s_ease-out_0s]
    }

    .shine-effect::before {
        content: '';
        position: absolute;
        left: -70px;
        top: -20px;
        width: 50px;
        height: 100px;

        background: #ffffff;
        background: linear-gradient(90deg, rgba(255, 255, 255, 0) 0%, rgb(255, 255, 255) 50%, rgba(255, 255, 255, 0) 100%);
        
        transform: rotateZ(30deg);
    }

    .shine-effect-mobile {
        animation: shine-reflex 1.3s ease-out 0s;
    }

    @keyframes shine-reflex {
        0% {
            opacity: .1;
        }
        50% {
            opacity: .9;
        }
        100% {
            opacity: .1;
            left: 100%;
        }
    }
</style>