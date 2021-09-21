<template>
  <p>{{ state.foo }} {{ state.bar }}</p>
</template>

<script>
import { defineComponent, reactive } from 'vue';

export default defineComponent({
  name: 'Reactve',
  setup() {
    const state = reactive({
      foo: 1,
      bar: 2,
    });

    state.foo = 5;

    return {
      state,
    };
  },
});
</script>
