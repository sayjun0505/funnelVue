<template>
  <button
    class="text-lg text-center rounded-lg hover:shadow-md hover:shadow-[#0c66ee]/50 transition duration-300"
    v-bind="$attrs"
    v-on="$listeners"
  >
    <slot></slot>
  </button>
</template>
<script>
export default {
  name: 'BaseButton',
  inheritAttrs: false,
}
</script>
