<template>
  <div class="switch">
    <button
      class="button"
      v-for="(visible, index) in visibleStanzas"
      :class="{ active: !visible }"
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

      if (visibleStanzasCount > 0 || visibleStanzasCount === 0) {
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
.button:nth-child(1){
  background-color: rgba(94, 202, 52, 0.946);
}
.button:nth-child(2){
  background-color: rgba(160, 110, 110, 0.955);
}
.button:nth-child(3){
  background-color: rgba(98, 102, 161, 0.98);
}
.button:nth-child(4){
  background-color: rgb(180, 78, 156);
}
.button {
  width: 20px;
  height: 20px;
  background-color: #f0f0f0;
  margin: 10px;
  border: none;
}

.active {
  width: 20px;
  height: 20px;
  margin: 10px;
}
.active:nth-child(1){
  background-color: rgba(94, 202, 52, 0.274);
}
.active:nth-child(2){
  background-color: rgba(160, 110, 110, 0.601);
}
.active:nth-child(3){
  background-color: rgba(98, 102, 161, 0.417);
}
.active:nth-child(4){
  background-color: rgba(180, 78, 156, 0.419);
}
</style>
