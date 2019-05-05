<template>
  <div class="grid-container">
    <div class="item1">1</div>
    <div class="item2">2</div>
    <div class="item3">3</div>
    <div class="item4">4</div>
    <div class="item5">5</div>
    <div class="item6">6</div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.grid-container {
  display: grid;
  grid-template-columns: auto auto auto;
  grid-gap: 10px;
  background-color: rgb(215, 240, 227);
  padding: 10px;
}

.grid-container > div {
  background-color: rgb(245, 229, 248);
  text-align: center;
  padding: 20px 0;
  font-size: 30px;	
}

</style>
