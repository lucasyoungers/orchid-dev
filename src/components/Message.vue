<template>
  <p>{{ message }}</p>
</template>

<script>
export default {
  name: 'Message',
  props: {
    message: String
  }
}
</script>