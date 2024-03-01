<script setup>
import Quatrain from "./components/Quatrain.vue"
</script>

<template>
  <div class="title">
    <h1>Invictus</h1>
    <h3 class="autor">by William Ernest Henley</h3>
  </div>
  <div class="verse">
    <Quatrain></Quatrain>
  </div>
</template>

<style scoped>
.title {
  display: flex;
  justify-content: center;
  align-items: baseline;
}
.title h1{
/* margin-right: 50px; */
}
.autor {
  margin-left: 20px;
}
.verse {
  display: flex;
  justify-content: center;
}
</style>
