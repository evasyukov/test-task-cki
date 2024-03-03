<template>
  <div class="switch">
    <button
      class="button"
      v-for="(visible, index) in visibleStanzas"
      :class="{ 'active': !visible }"
      :key="index"
      @click="toggleVisibility(index)"
    ></button>
  </div>
</template>

<script>
export default {
  props: {
    visibleStanzas: {
      type: Array,
      required: true,
    },
  },
  methods: {
    toggleVisibility(index) {
      const visibleStanzasCount = this.visibleStanzas.filter(
        (visible) => visible).length
      if (
        visibleStanzasCount > 1 ||
        (visibleStanzasCount === 1 && !this.visibleStanzas[index])
      ) {
        this.$emit("toggle", index)
      }
    },
  },
}
</script>

<style>
.switch {
  display: flex;
  height: 5vh;
  position: relative;
  right: 50px;
}
.button {

  width: 20px;
  height: 20px;
  background-color: #000; /* #000 */
  margin: 10px;
  border: none;
}

.active {
  width: 20px;
  height: 20px;
  background-color: #f0f0f0; /* #000 */
  margin: 10px;
  border: 2px solid #000;
}
</style>