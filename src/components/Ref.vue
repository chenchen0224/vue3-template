<template>
  <fragment
    ><div>ref:{{ counterRef }}</div>
    <div>state:{{ state.c }}</div>
  </fragment>
</template>

<script>
import { defineComponent, ref, reactive } from 'vue';

export default defineComponent({
  name: 'Ref',
  setup() {
    const counterRef = ref(0);
    const state = reactive({
      c: counterRef,
    });
    counterRef.value = 2;

    return {
      counterRef,
      state,
    };
  },
});
</script>
