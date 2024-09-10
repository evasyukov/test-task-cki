<template>
  <div class="title">
    <h1>Invictus</h1>
    <h3 class="autor">by William Ernest Henley</h3>
  </div>
  <div class="verse">
    <SwitchButtonVue
      :visibleStanzas="visibleStanzas"
      @toggle="toggleStanzaVisibility"
    />
    <Quatrain :visibleStanzas="visibleStanzas" />
  </div>
</template>

<script>
import Quatrain from "./components/Quatrain.vue"
import SwitchButtonVue from "./components/SwitchButton.vue"

export default {
  components: {
    Quatrain,
    SwitchButtonVue,
  },
  data() {
    return {
      visibleStanzas: [true, true, true, true],
    }
  },
  methods: {
    toggleStanzaVisibility(index) {
      this.visibleStanzas[index] = !this.visibleStanzas[index]
    },
  },
}
</script>

<style>
.title {
  display: flex;
  justify-content: center;
  align-items: baseline;
}
.autor {
  margin-left: 20px;
}
.verse {
  display: flex;
  justify-content: center;
}
</style>
