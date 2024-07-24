<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h1>
      没起名的盒子猫
    </h1>
  
    <h3>猫窝建设中…</h3>
    <h3>今天有在努力生自己吗？（没有）</h3>

    <div style="height: 24px;"></div>

    <h3><a href="https://space.bilibili.com/445016511">哔哩哔哩主页</a></h3>
    <h3><a href="https://live.bilibili.com/21512984">哔哩哔哩直播间</a></h3>
    <h3><a href="about:blank" style="cursor: not-allowed;">GitHub</a></h3>
    <h3><a href="about:blank" style="cursor: not-allowed;">Pixiv</a></h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
