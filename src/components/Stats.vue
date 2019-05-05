<template>
  <div class="stats">
    <h1>'L E F T'</h1>
    <EnemyItems />
    <pre> store.$state.AD: {{ $store.state.AD  }}</pre>
  </div>
</template>

<script>

import EnemyItems from "@/components/EnemyItems.vue";
import { mapGetters } from 'vuex'

export default {
  name: 'Stats',
    components: {
    EnemyItems
  },
  computed: {
    ...mapGetters([
      'countLinks',
    ]),
  }
}
</script>