<template>
  <div class="flex flex-row gap-2">
    <img :src="require(`~/assets/img/getting-started/${step.img}`)" class="max-w-[245px] mx-auto" alt="" />
    <div class="flex flex-col ml-8 w-[250px] justify-center leading-10">
      <p class="text-lg text-gray-700 leading-relaxed">
        {{ step.description }}
      </p>
      <h3 class="text-xl mt-8 text-neutral-800 font-semibold">{{ step.title }}</h3>
    </div>
  </div>
</template>
<script>
export default {
  name: 'LandingStep',
  props: {
    step: {
      type: Object,
      required: true,
    },
  },
}
</script>
