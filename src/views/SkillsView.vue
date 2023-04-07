<script setup lang="ts">
import ProjectList from "../components/ProjectList.vue";
</script>

<template>
  <div class="details">
    <ProjectList />
    <div class="intro">
      More can be found at my
      <a href="https://github.com/roryhofland/roryhofland.github.io"
        >Github page</a
      >.
    </div>
  </div>
</template>

<style>
.intro {
  margin-top: 2rem;
  margin-bottom: 3rem;
}

@media (min-width: 1024px) {
  .intro {
    text-align: center;
  }
}
</style>
