<template>
  <!-- <Reactve /> -->
  <WhyRef />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
// import Reactve from '@/components/Reactve.vue'
import WhyRef from '@/components/WhyRef.vue';

export default defineComponent({
  name: 'Home',
  components: {
    // Reactve,
    WhyRef,
  },
});
</script>
