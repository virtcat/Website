<script setup lang="ts">
import Table from './Table.vue';

defineProps<{}>()
</script>

<template>
  <div class="page">
    <div class="card">
      <div class="avatar">
        <img alt="Avatar" class="avatar-img" src="../assets/avatar.webp"/>
      </div>

      <h1 style="font-weight: 700; color: var(--color-primary);">
        Undefined_AI<div class="h1-cursor"/>
      </h1>
      <p>没起名的盒子猫</p>
      <p>猫窝建设中…</p>
      <p>今天有在努力生自己吗？（没有）</p>

      <div class="link-wrapper">
        <a class="link" target="_blank" href="https://space.bilibili.com/445016511">
          哔哩哔哩主页
        </a>
        <a class="link" target="_blank" href="https://live.bilibili.com/21512984">
          哔哩哔哩直播间
        </a>
        <a class="link" target="_blank" style="width: 4.2rem;" href="https://github.com/virtcat">
          GitHub
        </a>
        <a class="link" target="_blank" style="width: 4.2rem;" href="https://www.pixiv.net/users/57682225">
          Pixiv
        </a>
        <a class="link" target="_blank" style="width: 4.2rem" href="mailto:i@awsl.link">
          Email
        </a>
        <a class="link" style="width: 9rem;">
          Q群：329119819
        </a>
      </div>
    </div>

    <div class="main">
      <h2>简介</h2>
      <p><span class="heimu" title="你知道的太多了">“你是一只猫娘……”</span></p>
      <p><span class="heimu" title="你知道的太多了">“快给我变！”</span></p>
      <p>……</p>
      <p style="font-size: 125%; font-style: italic; font-weight: bold; color: var(--color-primary); opacity: 0.7;">[TBD]</p>

      <h2>资料</h2>
      <Table/>

      <h2>技能</h2>
      <p style="font-size: 125%; font-style: italic; font-weight: bold; color: var(--color-primary); opacity: 0.7;">[TBD]</p>
    </div>
  </div>
</template>

<style scoped>
.page {
  margin: 0 auto;
  min-width: 280px;
}

h1 {
  font-weight: 600;
  font-size: 2rem;
  position: relative;
  text-align: center;
}

h2 {
  font-weight: 550;
  font-size: 1.5rem;
  margin-top: 0.5rem;
}

h3 {
  font-weight: 550;
  font-size: 1.25rem;
  margin-top: 0.25rem;
}

p {
  margin: 4px 0;
}

.h1-cursor {
  display: inline-block;
  position: relative;
  width: 0.5em;
  height: 0.15em;
  top: 0.15em;
  background-color: #aaaaaa;
  animation: blink 2s linear infinite;
}

@keyframes blink {
  0%, 40% {
    opacity: 1.0;
  }
  50%, 90% {
    opacity: 0.2;
  }
  100% {
    opacity: 1.0;
  }
}

.avatar {
  display: block;
  margin: 16px auto;
  width: calc(128px + 2 * 8px);
  height: calc(128px + 2 * 8px);
  position: relative;
  border-radius: 50%;
  border: var(--color-primary) 2px solid;

  &::before {
    content: "";
    position: absolute;
    top: 4px;
    left: 4px;
    width: calc(128px + 2 * 2px);
    height: calc(128px + 2 * 2px);
    border-radius: 50%;
    border: var(--color-primary) 3px dotted;
    animation: animate-rotate 60s linear infinite;
  }
}

@keyframes animate-rotate {
  100% {
    transform: rotate(1turn);
  }
}

.avatar-img {
  width: 128px;
  height: 128px;
  position: absolute;
  top: 6px;
  left: 6px;
  border-radius: 50%;
}

.card {
  padding: 16px 0;
  border-radius: 8px;
  background-color: #99999922;
}

.card p {
  text-align: center;
}

.link-wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 24em;
  margin: 0 auto;
}

.link {
  display: block;
  width: 8.8em;
  text-align: center;
  font-size: 0.9em;
  font-weight: bold;
  border-radius: 1.2em;
  border: 2px solid var(--color-primary);
  box-sizing: border-box;
  margin: 4px;

  &:hover {
    background-color: var(--color-primary);
    color: var(--color-background);
  }
}

.link-disabled {
  font-style: italic;
  cursor: not-allowed;
  pointer-events: none;
  text-decoration: line-through;
  opacity: 0.4;
}


@media (min-width: 960px) {
  .page {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .card {
    margin-right: 2rem;
  }
}
</style>
