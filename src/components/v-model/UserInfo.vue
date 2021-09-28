<template>
  <input :value="name" @input="$emit('update:name', $event.target.value)" />
</template>

<script>
export default {
  name: 'UserInfo',
  props: {
    name: String
  }
}
</script>
