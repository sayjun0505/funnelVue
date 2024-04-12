<template>
  <div class="w-full lg:w-1/3 lg:mt-0 overflow-hidden space-y-6" v-bind="$attrs">
    <div class="w-full flex-col">
      <div class="w-full rounded-full w-20 h-20 flex flex-start">
        <div
          v-for="data in datasets"
          :key="data.id"
          class="w-20 h-20 drop-shadow-2xl rounded-full relative overflow-hidden"
        >
          <img
            :src="require(`~/assets/img/crypto-icon/${data.logo}`)"
            alt=""
            class="bg-blue-600 w-40 h-20 p-5 absolute top-0 left-0"
          />
        </div>
      </div>
    </div>
    <div class="flex flex-col px-8">
      <h1 class="text-bold text-3xl text-center">{{ title }}</h1>
      <div class="overflow-x-auto sm:-mx-6 lg:-mx-8">
        <div class="text-center px-2 sm:px-6 py-2 align-middle inline-block min-w-full overflow-hidden">
          <p>{{ description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'LandingCryptoStatistic',
  props: {
    title: {
      type: String,
      default: '',
    },
    description: {
      type: String,
      default: '',
    },
    datasets: {
      type: Array,
      default: () => [],
    },
  },
}
</script>
