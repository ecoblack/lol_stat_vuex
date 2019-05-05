<template>
  <div class="champion-container">
    <div class="avatar">
      <img :src="imgName">
    </div>
    <div>
      <div class="stats-container">
        <div class="item">
          <p>
            Attack Damage:
            <br>
            {{ $store.state.AD }}
          </p>
        </div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
        <div class="item">5</div>
        <div class="item">6</div>
        <div class="item">7</div>
        <div class="item">8</div>
        <div class="item">7</div>
        <div class="item">8</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Champion",
  computed: {
    imgName: function() {
      var activeChampion = this.$store.state.activeChampion;
      if (activeChampion === "") {
        return "";
      } else {
        var imgPath = "/img/champion/tiles/" + activeChampion + "_0.jpg";
        return imgPath;
      }
    },
    baseAd: function() {
        var baseAd = this.$store.state.baseAd;
    }
  },
  methods: {}
  //   watch: {
  //     activeChampion: function(newSelected) {
  //       console.log(`watch triggered, value of selected is: ${newSelected}`);
  //       axios
  //         .get("../champion.json")
  //         .then(
  //           response =>
  //             (this.entity = response.data.data[`${activeChampion}`]["stats"])
  //         );
  //     },
  //     level: function(newLevel) {
  //       console.log(`watch triggered. New level is ${newLevel}`);
  //     }
  //   }
};
</script>

<style scoped>
.champion-container {
  padding: 80px 40px;
  /* left: 10%;
  height: 25%; */
  /* position: absolute; */
  border-style: solid;
  border-width: 5px;
  border-color: aqua;
}

body {
}
.stats-container {
  display: grid;
  grid-template-columns: auto auto;
  padding: 10px;
  border-radius: 2px;
}
.item {
  background-color: #80cbc4;
  border: 1px solid #fff;
  padding: 20px;
  font-size: 30px;
  text-align: left;
}
</style>
