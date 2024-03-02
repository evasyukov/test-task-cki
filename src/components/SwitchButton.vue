<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    index: {
      type: Number,
      required: true,
    },
    stanza: {
      type: Object,
      required: true,
    },
  },
  methods: {
    toggleVisibility() {
      this.$emit("toggle", this.index)
    },
  },
}
</script>

<template>
  <div class="switch">
    <button @click="toggleVisibility" class="button">{{ label }}</button>
  </div>
</template>

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
  background-color: #ffffffdc; /* #000 */
  margin: 10px;
  border: none;
}

.button:active {
  background-color: #000;
}
</style>
