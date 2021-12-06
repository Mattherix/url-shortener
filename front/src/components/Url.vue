<template>
  <p>{{ id }}</p>
</template>

<script>
export default {
  name: 'Url',
  props: {
    id: Number
  },
  data() {
    return {
      url: '',
      password: ''
    }
  }
}
</script>

<style>
</style>
