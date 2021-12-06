<template>
  <div class="grid place-items-center">
    <Input @newUrl="onNewUrl" />
    <ul v-for="item in localStorageList" :key="item">
      <div v-if="!isNaN(Number(item))">
        <Url :id="Number(item)" />
      </div>
    </ul>
  </div>
</template>

<script>
import Input from './components/Input.vue'
import Url from './components/Url.vue'
import './assets/tailwind.css'

function localStorageItems() {
  let ans = []
  for (let i = 0; i < localStorage.length; i++) {
    ans.push(localStorage.key(i))
  }
  console.log(ans)
  return ans
}

export default {
  name: 'App',
  components: {
    Input,
    Url
  },
  data() {
    return {
      item: 0,
      localStorageList: localStorageItems() 
    }
  }, 
  methods: {
    onNewUrl() {
      this.localStorageList = localStorageItems()
    }
  }
}
</script>

<style>
</style>
