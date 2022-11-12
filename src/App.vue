<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import MainHeader from "./components/MainHeader.vue";
import MainFooter from "./components/MainFooter.vue";
</script>

<template>
  <header>
    <div class="wrapper">
      <MainHeader />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/skills">Projects</RouterLink>
        <RouterLink to="/about">About Me</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </div>
  </header>

  <div class="router-wrapper">
    <RouterView v-slot="{ Component }">
      <Transition name="fade" mode="out-in">
        <component :is="Component" />
      </Transition>
    </RouterView>
  </div>

  <footer>
    <MainFooter />
  </footer>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

header {
  line-height: 1.5;
  max-height: 100vh;
  width: 100%;
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  color: var(--color-text);
  width: 100%;
  font-size: 12px;
  text-align: center;
}

nav a.router-link-exact-active {
  color: hsla(160, 100%, 37%, 1);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
  color: var(--color-text);
}

nav a:first-of-type {
  border: 0;
}

h3 {
  color: white;
}
.router-wrapper {
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
  }
}
</style>
