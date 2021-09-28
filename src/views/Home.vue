<template>
  <!-- <Reactve /> -->
  <!-- <WhyRef /> -->
  <VModel />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
// import Reactve from '@/components/Reactve.vue'
// import WhyRef from '@/components/WhyRef.vue'
import VModel from '@/components/v-model/index.vue'

export default defineComponent({
  name: 'Home',
  components: {
    // Reactve,
    // WhyRef,
    VModel
  }
})
</script>
