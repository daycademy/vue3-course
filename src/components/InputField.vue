<template>
  <label class="text-base text-gray-500">
    {{ placeholder }}
  </label>
  <input
    v-bind="$attrs"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    class="w-full px-3 py-2 leading-tight text-gray-700 border rounded shadow appearance-none focus:outline-none focus:shadow-outline"
    :placeholder="placeholder"
  >
</template>

<script>
export default {
  props: {
    placeholder: {
      type: String,
      default: '',
    },
    modelValue: {
      type: String,
      default: '',
    },
  },
};
</script>
