<script setup lang="ts">
    const props = defineProps(['project']);
</script>

<template>
    <div class="w-[15rem] flex flex-col justify-start items-center bg-neutral-400 rounded-2xl overflow-hidden">
        <div class="w-full h-44 bg-neutral-500">
            <img :src="'projects/'+ props.project.project_image + '.png'"
        </div>
        <div class="w-full h-48 p-[2.5px] bg-gradient-to-r from-neutral-900 to-neutral-700">
            <div class="w-full h-full flex flex-col justify-between items-start bg-neutral-800 rounded-b-xl px-5 py-4">
                <div class="space-y-2">
                    <p class="font-poppins font-semibold text-white text-lg">
                        {{ props.project.name }}
                    </p>
                    <p class="font-poppins font-light text-[11px] text-neutral-500 leading-3">
                        {{ props.project.description.slice(0, 150) + '...' }}
                    </p>
                </div>
                <div class="w-full flex justify-between items-center">
                    <div class="flex gap-x-2 items-center">
                        <p class="font-poppins text-xs text-neutral-400">Online</p>
                        <span class="w-2 h-2 bg-green-500 rounded-full"></span>

                    </div>
                    <NuxtLink
                        :to="props.project.project_link"
                        target="_blank"
                        class="flex gap-1 items-center bg-gradient-to-r from-neutral-300 from-75% to-neutral-500 px-2.5 py-1 rounded-xl font-poppins font-semibold text-xs"
                    >
                        Acessar
                        <IconsArrowForward width="18" height="18" stroke="#000" />
                    </NuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>