<template>
  <div class="flex items-center justify-center h-full">
    <div class="px-12 py-10 bg-white rounded-lg shadow-2xl">
      <Form v-model:firstname="myFirstname" v-model:lastname="myLastname" />

      <p class="mt-4 text-gray-700">
        Vorname: {{ myFirstname }}
      </p>
      <p class="mt-1 text-gray-700">
        Nachname: {{ myLastname }}
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Form from '@/components/Form.vue';

@Options({
  components: {
    Form,
  },
})
export default class Home extends Vue {
  myFirstname = '';

  myLastname = '';
}
</script>
