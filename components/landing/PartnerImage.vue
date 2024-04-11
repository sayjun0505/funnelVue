<template>
  <div class="w-full lg:w-1/3 mt-6 mb-10 lg:mt-0 overflow-hidden space-y-6">
    <div class="w-full flex items-center justify-normal">
      <div class="border-b border-gray-200">
        <img :src="require(`~/assets/img/partner/faq.png`)" alt="" class="bg-blue-600 w-16 h-16 p-3 rounded-3xl mr-3"/>
      </div>
      <h1 class="text-2xl">{{ query.title }}</h1>      
    </div>
    <div class="flex flex-col">
      <div class="-my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
        <div class="px-2 sm:px-6 py-2 align-middle inline-block min-w-full overflow-hidden">
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
