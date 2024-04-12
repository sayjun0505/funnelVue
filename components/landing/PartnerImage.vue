<template>
  <div class="w-full flex flex-row lg:w-1/3 mt-6 mb-10 lg:mt-0 overflow-hidden space-y-6">
    <div class="w-[200px] flex flex-start">
      <img :src="require(`~/assets/img/partner/faq.png`)" alt="" class="w-16 h-12 mr-3" />
    </div>
    <div class="flex flex-col items-start">
      <h1 class="text-2xl">{{ query.title }}</h1>
      <div class="overflow-x-auto text-left mt-4">
        <div class="align-middle inline-block min-w-full overflow-hidden">
          <p>{{ query.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'LandingPartnerImage',
  props: {
    query: {
      type: Object,
    },
  },
}
</script>
