<template>
  <InputField
    placeholder="Vorname"
    :modelValue="firstname"
    @input="$emit('update:firstname', $event.target.value)"
    type="text"
    class="mb-4"
  />
  <InputField
    placeholder="Nachname"
    :modelValue="lastname"
    @input="$emit('update:lastname', $event.target.value)"
  />
</template>

<script>
import InputField from '@/components/InputField.vue';

export default {
  props: {
    firstname: {
      type: String,
      default: '',
    },
    lastname: {
      type: String,
      default: '',
    },
  },
  components: {
    InputField,
  },
};
</script>
