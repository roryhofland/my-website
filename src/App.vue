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
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </div>
  </header>

  <div class="router-wrapper">
    <div class="inner-wrapper">
      <RouterView v-slot="{ Component }">
        <Transition name="fade" mode="out-in">
          <component :is="Component" />
        </Transition>
      </RouterView>
    </div>
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
  justify-content: center;
  padding: 0;
}

.wrapper {
  justify-content: center;
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
  font-size: 36px;
  visibility: hidden;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
    justify-content: center;
  }

  .router-wrapper {
    display: block;
  }
  .inner-wrapper {
    margin: auto;
    max-width: 1280px;
  }

  nav {
    font-size: 1rem;
    padding: 1rem 0;
  }
}
</style>
