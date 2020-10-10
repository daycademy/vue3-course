<template>
  <input
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    class="w-full px-3 py-2 leading-tight text-gray-700 border rounded shadow appearance-none focus:outline-none focus:shadow-outline"
  >
</template>

<script>
export default {
  props: {
    modelValue: {
      type: String,
      default: '',
    },
  },
};
</script>
