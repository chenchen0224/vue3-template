<template>
  <div>foo: {{ foo }}，numb: {{ numb }}</div>
</template>

<script>
import { defineComponent, computed } from 'vue';

export default defineComponent({
  name: 'WhyRef',
  setup() {
    let foo = 1;

    setTimeout(() => {
      console.log('setTimeout');
      foo = 3;
    }, 1000);
    (() => {
      console.log('x');
      foo = 2;
    })();

    const numb = computed(() => foo + 5);

    return {
      foo,
      numb,
    };
  },
});
</script>
