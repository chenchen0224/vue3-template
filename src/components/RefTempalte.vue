<template>
  <p ref="domRef">我是一个p标签</p>
</template>

<script>
import { defineComponent, ref, onMounted } from 'vue';

export default defineComponent({
  name: 'RefTempalte',
  setup() {
    const domRef = ref(null);

    onMounted(() => {
      console.log(domRef.value, domRef.value.innerHTML);
    });

    return {
      domRef,
    };
  },
});
</script>
