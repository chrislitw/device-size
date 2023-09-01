<script setup>
import { ref } from "vue";

const ww = ref(window.innerWidth);
const hh = ref(window.innerHeight);
</script>

<template>
  <div class="corner">
    <div class="dot tl"></div>
    <div class="dot tr"></div>
    <div class="dot br"></div>
    <div class="dot bl"></div>
  </div>
  <div class="data">
    <span>innerWidth: {{ ww }}</span>
    <span>innerHeight: {{ hh }}</span>
  </div>
</template>

<style>
#app {
  width: 100vw;
  height: 100dvh;
  background-color: antiquewhite;
}

.dot {
  position: absolute;
  width: 10px;
  height: 10px;
  background-color: navy;
}

.tl {
  top: 0;
  left: 0;
}

.tr {
  top: 0;
  right: 0;
}

.br {
  bottom: 0;
  right: 0;
}

.bl {
  bottom: 0;
  left: 0;
}

.data {
  display: flex;
  flex-direction: column;
  gap: 12px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  margin: auto;
}
</style>
