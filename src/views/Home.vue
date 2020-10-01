<template>
  <div class="h-full flex items-center justify-center">
    <Button @click="showNotification">
      Klick mich
    </Button>
  </div>

  <transition
    enter-active-class="transition-all ease-in-out duration-300"
    leave-active-class="transition-all ease-in-out duration-300"
    enter-from-class="opacity-0"
    leave-to-class="opacity-0"
  >
    <div
      v-if="isNotificationVisible"
      class="absolute mt-4 ml-4 px-4 py-2 top-0 left-0 bg-white rounded-lg shadow-2xl text-sm"
    >
      Button wurde geklickt!
    </div>
  </transition>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Button from '@/components/Button.vue';

@Options({
  components: {
    Button,
  },
})
export default class Home extends Vue {
  private isNotificationVisible = false;

  private showNotification(payload: { duration: number }): void {
    this.isNotificationVisible = true;

    setTimeout(() => {
      this.isNotificationVisible = false;
    }, payload.duration);
  }
}
</script>
