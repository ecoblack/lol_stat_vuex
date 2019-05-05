<template>
  <div class="home">
    <Champion />
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
import Champion from '@/components/Champion.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    Runes,
    Level,
    Champion
  }
}
</script>
