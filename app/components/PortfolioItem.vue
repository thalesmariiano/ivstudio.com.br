<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    src: string
    name: string
    categories: string[]
    alt?: string
    wrapperClass?: string
    imgClass?: string
  }>(),
  {
    alt: undefined,
    wrapperClass: '',
    imgClass: '',
  },
)

const categoriesLabel = computed(() => (props.categories?.length ? props.categories.join(' · ') : ''))
</script>

<template>
  <div
    tabindex="0"
    :class="[
      'group relative overflow-hidden focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-white/60 focus-visible:ring-offset-0',
      wrapperClass,
    ]"
  >
    <img
      :src="src"
      :alt="alt ?? name"
      :class="[
        'w-full h-full object-cover transition-transform duration-300 ease-out group-hover:scale-105',
        imgClass,
      ]"
    />

    <div
      :class="[
        'pointer-events-none absolute inset-0 opacity-0 transition-opacity duration-300 ease-out',
        'group-hover:opacity-100 group-focus-visible:opacity-100',
      ]"
    >
      <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/35 to-transparent" />
      <div class="absolute bottom-0 left-0 right-0 p-4 sm:p-5">
        <p v-if="categoriesLabel" class="font-poppins text-white/80 text-xs sm:text-sm tracking-[3px] uppercase">
          {{ categoriesLabel }}
        </p>
        <h3 class="font-poppins text-white text-xl sm:text-2xl font-semibold leading-tight">
          {{ name }}
        </h3>
      </div>
    </div>
  </div>
</template>

