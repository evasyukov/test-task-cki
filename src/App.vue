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

  <div class="change-theme">
    <button @click="changeTheme">Сменить тему</button>
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
    changeTheme() {
      const bodyClass = document.querySelector("body")

      if (bodyClass.className.includes("dark-theme")) {
        bodyClass.classList.remove("dark-theme")
        bodyClass.classList.add("light-theme")
      } else {
        bodyClass.classList.remove("light-theme")
        bodyClass.classList.add("dark-theme")
      }
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
.change-theme button{
  background-color: transparent;
  color: #1206f6;
  border: 1px solid #1206f6; 
  padding: 10px 15px; 
  cursor: pointer; 
  position: absolute;
  top: 30px;
  left: 270px;
}
</style>
