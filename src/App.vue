<script setup>
import Quatrain from './components/Quatrain.vue';


</script>

<template>
  <div class="title">
    <h1 class="verse">Invictus</h1>
    <h3 class="autor">by William Ernest Henley</h3>
  </div>
  <Quatrain></Quatrain>
</template>

<style scoped>
.title {
  display: flex;
  justify-content: center;
}

.autor {
  padding-left: 5vh;
}
</style>
