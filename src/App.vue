<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <img alt="Avatar" class="logo" src="./assets/avatar.webp" width="125px" height="125px" />

    <div class="wrapper">
      <HelloWorld msg="Undefined_AI" />
    </div>
  </header>

  <!-- <main>
    <div>This is main part.</div>
  </main> -->
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
  border-radius: 50%;
  border: 2px solid gray;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    /* padding-right: calc(var(--section-gap) / 2); */
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
