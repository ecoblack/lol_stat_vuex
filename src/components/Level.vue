<template>
  <div class="container">
    <div class="level">
      <select  v-model="$store.state.activeChampion">
        <option disabled value>Select a champion</option>
        <option v-for="champion in champions" :value="champion.name">
          {{ champion.name }}
          </option>
      </select>

      <pre>store.$state.activeChampion: {{ $store.state.activeChampion  }}</pre>

      <br>
      
    </div>
    <div>
      <span>
       <pre> store.$state.level: {{ $store.state.level  }}</pre>
     
      <button @click="increment(18)">+</button>
      <button @click="decrement(1)">-</button>
    </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Level",
  data() {
    return {
      champions: [
        {
          id: "1",
          name: "Shen",
          data: {
            ad: 24
          }
        },
        {
          id: "2",
          name: "Janna"
        },
        {
          id: "3",
          name: "Yasuo"
        }
      ]
    };
  },
  computed: {
    level: function() {
      return this.$store.getters.level;
    }
  },
  methods: {
    increment(limit) {
      this.$store.commit("increment", limit);
    },
    decrement(limit) {
      this.$store.commit("decrement", limit);
    },
    setActiveChampion(val) {
      this.$store.commit("setActiveChampion", val);
    }
  }
};
</script>

<style scoped>
html,
body {
  height: 100%;
}

.container {
  position: absolute;
  top: 50%;
  left: 50%;
  box-shadow: 0 0 25px rgba(0, 0, 0, 0.08);
  transform: translateX(-50%) translateY(-50%);
  width: 300px;
  height: 200px;
  padding-bottom: 20px;
}

.counter {
  text-align: center;
  font-size: 40px;
  margin-bottom: 15px;
  color: #4b1248;
}

button {
  /*   margin-right: 5px; */
  padding: 10px 15px;
  font-size: 20px;
  background-image: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%);
  border: 1px solid #8fd3f4;
  outline: none;
}

button:hover {
  opacity: 0.8;
  cursor: pointer;
}

.actions-inner {
  display: flex;
  justify-content: center;
}
</style>
