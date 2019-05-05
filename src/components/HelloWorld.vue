<template>
  <div class="hello">
    <div class="left">
      <h1>Left</h1>
      
      <h3>{{ AD }}</h3>
      <!-- <p>{{ runes }}</p> -->
    </div>
    <div class="right">
      <stats/>
    </div>
  </div>
</template>

<script>
import Stats from "@/components/Stats.vue";
import { mapState, mapMutations } from "vuex";

export default {
  name: "HelloWorld",
  components: {
    Stats
  },
  data() {
    return {
      newLink: ""
    };
  },
  computed: {
    ...mapState(["title", "AD", "links", "runes"])
    // Other properties
  },
  methods: {
  }
};
</script>

<style>
html,
#app,
.home {
  height: 100%;
}
body {
  background-color: #f4f4f4;
  margin: 0;
  height: 100%;
}

.hello {
  display: grid;
  grid-template-columns: repeat(2, 50%);
  grid-template-rows: 100%;
  grid-template-areas: "left right";
  height: 100%;
}

.left,
.right {
  padding: 30px;
}

ul {
  list-style-type: none;
  padding: 0;
}
ul li {
  padding: 20px;
  background: white;
  margin-bottom: 8px;
}

.right {
  grid-area: right;
  background-color: #e9e9e9;
}

input {
  border: none;
  padding: 20px;
  width: calc(100% - 40px);
  box-shadow: 0 5px 5px lightgrey;
  margin-bottom: 50px;
  outline: none;
}
</style>