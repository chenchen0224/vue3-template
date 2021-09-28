<template>
  <p>{{ name }}</p>

  <user-info v-model:name="name"></user-info>
  <!-- 相当于 -->
  <!-- :name="name" @update:name="name = $event" -->
</template>

<script>
import { reactive, toRefs } from 'vue'
import UserInfo from './UserInfo.vue'

export default {
  name: 'VModel',
  components: { UserInfo },
  setup() {
    const state = reactive({
      name: 'chen'
    })

    return toRefs(state)
  }
}
</script>
