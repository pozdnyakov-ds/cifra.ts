<template>
  <div>
    <p>Wellcome!</p>
    <p>{{ framework.name }} -> {{ framework.version }} -> {{ newVersion }}</p>
    <button class="btn" @click="change">Change</button>
    <ul>
      <li>Home page</li>
      <li><nuxt-link to="/about">About</nuxt-link></li>
    </ul>
  </div>
</template>

<script lang="ts">
import { ref, reactive, computed } from '@nuxtjs/composition-api'

export default {
  setup(context: any) {
    const name = ref('Vue JS')
    const version = ref(3)

    const framework = reactive({
      name: 'Vue JS',
      version: 3
    })

    const newVersion = computed(() => { 
      return framework.version = framework.version * 10
    })

    function changeInfo() { 
      framework.name = framework.name + "+"
      framework.version++
      console.log("Router: ", context)
    }

    return {
      framework,
      change: changeInfo,
      newVersion
    }  
  }
}
</script>

<style scoped>

</style>