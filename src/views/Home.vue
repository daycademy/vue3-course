<template>
  <div class="flex items-center justify-center h-full">
    <div class="px-12 py-10 bg-white rounded-lg shadow-2xl">
      <InputField v-model="myInput" />

      <p class="mt-4 text-gray-700">
        Input: {{ myInput }}
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import InputField from '@/components/InputField.vue';

@Options({
  components: {
    InputField,
  },
})
export default class Home extends Vue {
  myInput = '';
}
</script>
