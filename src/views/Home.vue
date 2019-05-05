<template>
  <div class="home">
    <HelloWorld />
    <Runes />
    <Level />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Runes from '@/components/Runes.vue'
import Level from '@/components/Level.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    Runes,
    Level
  }
}
</script>
