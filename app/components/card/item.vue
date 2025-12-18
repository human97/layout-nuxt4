<script setup lang="ts">

const props = defineProps({
    card: {
        type: Object,
        default: () => ({
            title: 'Консультация и помощь иностранным гражданам в подготовке заявления на разрешение на временное проживание (РВП) и вида на жительство (ВНЖ) в РФ',
        }),
    },
})
</script>

<template>
    <div class="gradient-border relative rounded-2xl p-2 lg:p-6 flex flex-col justify-between min-h-[140px] md:min-h-[174px] lg:min-h-[308px]">
        <nuxt-link
            to="/"
            class="absolute top-2 right-2 lg:top-6 lg:right-6"
        >
            <img
                src="~/assets/icon/link.svg"
                alt="link"
                class="size-4 lg:size-12 text-white"
            />
        </nuxt-link>

        <h2 class="text-sm lg:text-2xl leading-[1.2] text-white mt-auto md:pr-5 lg:pr-10">
            {{ card.title }}
        </h2>
    </div>
</template>

<style scoped>
.gradient-border {
  border: 1px solid transparent;
  background: linear-gradient(#35335a, #35335a 0) padding-box, linear-gradient(to left, #FFFFFF80, #FFFFFF14) border-box;
}
</style>