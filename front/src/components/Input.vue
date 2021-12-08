<template>
  <input
    placeholder="Collez le lien que vous voulez réduire"
    class="my-3 p-4 w-10/12 text-3xl text-center rounded-full bg
    focus:outline-none focus:ring-8 focus:ring-blue-400 focus:ring-opacity-50 focus:shadow-lg" 
    v-model="url" @keyup.enter="shorten"/>
</template>

<script>
export default {
  name: 'Input',
  emits: ["newUrl"],
  data() {
    return {
      id: 0,
      url: '',
      password: ''
    }
  },
  methods: {
    shorten() {
      /* Send a request to get the shorten link */
      this.id = Math.floor((Math.random() * 10000) + 1)
      var data = {
        url: this.url,
        password: this.password
      }
      localStorage.setItem(this.id, JSON.stringify(data))
      this.url = ''

      this.$emit('newUrl', this.id.toString())
    }
  }
}
</script>

<style>
</style>
