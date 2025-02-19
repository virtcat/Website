<script setup lang="ts">
</script>

<template>
  <div class="table">
    <div class="row">
      <div class="title">本名</div>
      <div class="content">？？？</div>
    </div>
    <div class="row">
      <div class="title">别名</div>
      <div class="content">Undefined_AI、盒子猫、无名</div>
    </div>
    <div class="row">
      <div class="title">年龄</div>
      <div class="content">？？？</div>
    </div>
    <div class="row">
      <div class="title">生日</div>
      <div class="content">？？？</div>
    </div>
    <div class="row">
      <div class="title">……</div>
      <div class="content">……</div>
    </div>
  </div>
</template>

<style lang="css" scoped>
.table {
  border: 1px solid #aaaaaa33;
  border-radius: 8px;

  --width1: 5em;
}

.row {
  margin: 6px;
}

.title {
  position: absolute;
  width: var(--width1);
  text-align: center;
  font-weight: bold;
  color: var(--color-primary);
}

.content {
  margin-left: var(--width1);
}
</style>
