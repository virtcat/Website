<script setup lang="ts">
import { onMounted, ref } from "vue";

const mode = ref(1);

function select(m: 0 | 1 | 2) {
  localStorage.setItem('theme-mode', m.toString());
  mode.value = m;
  if (m == 1) {
    autoMode();
  } else {
    enableDark(m == 2);
  }
}

onMounted(() => {
  try {
    window.matchMedia("(prefers-color-scheme: dark)").addEventListener("change", autoMode);
    let saved = localStorage.getItem('theme-mode');
    if (saved !== null) {
      let m = parseInt(saved);
      if (m == 0 || m == 1 || m == 2) {
        select(m);
      }
    }
  } catch (e) {}
});

function autoMode() {
  if (mode.value != 1) return;
  if (window.matchMedia("(prefers-color-scheme: dark)").matches) {
    enableDark(true);
  } else {
    enableDark(false);
  }
}

function enableDark(dark: boolean) {
  const root = document.documentElement;
  if (dark) {
    root.classList.add('dark');
  } else {
    root.classList.remove('dark');
  }
}
</script>

<template>
  <div class="theme-switch">
    <div @click="select(0)" class="option" :class="{ selected: mode == 0 }">
      <img src="./icons/sun.svg" class="svg"/>
    </div>
    <div @click="select(1)" class="option" :class="{ selected: mode == 1 }">
      <div class="auto">Auto</div>
    </div>
    <div @click="select(2)" class="option" :class="{ selected: mode == 2 }">
      <img src="./icons/moon.svg" class="svg"/>
    </div>
  </div>
</template>

<style lang="css" scoped>
.theme-switch {
  height: 36px;
  width: 94px;
  border-radius: 18px;
  display: flex;
  align-items: center;
  justify-content: center;
  
  background-color: var(--color-background);
  border: 1px solid #99999999;
}

.option {
  position: relative;
  height: 24px;
  width: 24px;
  text-align: center;
  margin: 2px;
  padding: 2px;
  line-height: 20px;
  border-radius: 50%;
  overflow: visible;
  
  &:hover {
    background-color: #aaaaaa66;
  }
}

.selected {
  background-color: #aaaaaa66;
}

.auto {
  user-select: none;
  width: fit-content;
  margin-left: 50%;
  transform: translateX(-50%) scaleX(0.6);
}

.dark .svg {
  filter: invert();
}
</style>
