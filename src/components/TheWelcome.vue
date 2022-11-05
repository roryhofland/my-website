<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'

</script>

<template>
  <template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
</template>
  <WelcomeItem>
    <template #icon>
      <i class="fa fa-home"></i>
    </template>
    <template #heading>Documentation</template>

    Vue’s
    <a href="https://vuejs.org/" target="_blank" rel="noopener">official documentation</a>
    provides you with all information you need to get started.
  </WelcomeItem>

  
</template>
