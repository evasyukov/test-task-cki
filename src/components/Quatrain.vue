<template>
  <SwitchButton></SwitchButton>
  <div class="quatrain">
    <div id="quatrain-one">
      <p>Out of the night that covers me,</p>
      <p>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Black as the pit from pole to pole,
      </p>
      <p>I thank whatever gods may be</p>
      <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;For my unconquerable soul.</p>
    </div>
    <div id="quatrain-two">
      <p>In the fell clutch of circumstance</p>
      <p>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I have not winced nor cried aloud.
      </p>
      <p>Under the bludgeonings of chance</p>
      <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;My head is bloody, but unbowed.</p>
    </div>
    <div id="quatrain-three">
      <p>Beyond this place of wrath and tears</p>
      <p>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Looms but the Horror of the shade,
      </p>
      <p>And yet the menace of the years</p>
      <p>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Finds and shall find me unafraid.
      </p>
    </div>
    <div id="quatrain-four">
      <p>It matters not how strait the gate,</p>
      <p>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; How charged with punishments the
        scroll,
      </p>
      <p>I am the master of my fate</p>
      <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I am the captain of my soul.</p>
    </div>
  </div>
</template>

<script setup>
import SwitchButton from "./SwitchButton.vue"
</script>

<style>
.quatrain {
  font-size: 24px;
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
}
.quatrain p {
  margin: 0;
}
.quatrain div {
  margin-bottom: 20px;
}
</style>
