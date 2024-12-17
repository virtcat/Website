<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="purple" style="font-weight: bold;">{{ msg }}</h1>
    <h1>
      没起名的盒子猫
    </h1>
  
    <p>猫窝建设中…</p>
    <p>今天有在努力生自己吗？（没有）</p>

    <div style="height: 24px;"></div>

    <a class="link" target="_blank" href="https://space.bilibili.com/445016511">哔哩哔哩主页</a>
    <a class="link" target="_blank" href="https://live.bilibili.com/21512984">哔哩哔哩直播间</a>
    <a class="link" target="_blank" href="https://github.com/virtcat">GitHub</a>
    <a class="link" target="_blank" href="https://www.pixiv.net/users/57682225">Pixiv （暂无作品）</a>
    <a class="link" target="_blank" href="mailto:i@awsl.link">Email</a>
    <a class="link">Q群：329119819</a>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.2rem;
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

.link {
  display: block;
  width: 200px;
  text-align: center;
  font-size: 1.0rem;
  height: 2.4rem;
  border-radius: 1.2rem;
  border: 2px solid var(--color-primary);
  box-sizing: border-box;
  margin: 8px auto;
}
.disabled {
  font-style: italic;
  cursor: not-allowed;
  pointer-events: none;
  text-decoration: line-through;
  opacity: 0.4;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }

  .link {
    margin: 8px 0;
  }
}
</style>
