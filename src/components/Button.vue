<template>
  <button
    type="button"
    class="
      px-12 py-10 text-xl rounded-lg bg-white shadow-2xl hover:shadow-lg
      hover:bg-gray-100 transition-all duration-300 ease-in-out focus:outline-none
    "
    @click="$emit('click', { duration: 2000 })"
  >
    <slot></slot>
  </button>
</template>

<script lang="ts">
import { Vue, Options } from 'vue-class-component';

@Options({
  emits: {
    click: (payload: { duration: number }) => !!(payload.duration),
  },
})
export default class Button extends Vue {}
</script>
