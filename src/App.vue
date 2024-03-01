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
}
.autor {
  padding-left: 5vh;
}
.verse {
  display: flex;
  justify-content: center;
}
</style>
