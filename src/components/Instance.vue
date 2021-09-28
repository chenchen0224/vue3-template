<template>
  <div ref="test">test</div>
</template>

<script lang="ts">
import { defineComponent, getCurrentInstance, onMounted } from 'vue'

export default defineComponent({
  name: 'Instance',
  data() {
    return {
      a: 1
    }
  },
  setup() {
    const instance = getCurrentInstance()
    if (instance) {
      console.log(111, instance.refs.test)
    }

    onMounted(() => {
      if (instance) {
        console.log('onMounted', instance.refs.test)
      }
    })
  }
})
</script>
