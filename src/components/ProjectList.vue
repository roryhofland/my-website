<script setup lang="ts">
import ProjectItem from "../components/ProjectItem.vue";
</script>

<template>
  <div class="list-wrapper">
    <ProjectItem>
      <template #icon>
        <a
          class="proj-img"
          target="_blank"
          href="https://github.com/ramp4-pcar4/ramp4-pcar4"
          ><img class="thumbnail" src="../assets/images/ramp.svg" alt=""
        /></a>
      </template>
      <template #heading>
        <a
          class="proj-title"
          target="_blank"
          href="https://github.com/ramp4-pcar4/ramp4-pcar4"
          >RAMP4</a
        >
      </template>
      <template #description>
        The Reusable Accessible Mapping Platform is a Javascript based web
        mapping platform that provides a reusable, responsive and WCAG 2.1 AA
        compliant common viewer for the Government of Canada.
      </template>
      <template #stack>
        <img src="../assets/icons/icons8-typescript.svg" alt="typescript" />
        <img src="../assets/icons/icons8-javascript.svg" alt="javascript" />
        <img src="../assets/icons/icons8-vue.svg" alt="vue" />
        <img src="../assets/icons/icons8-tailwind-css.svg" alt="tailwind-css" />
      </template>
    </ProjectItem>
    <ProjectItem>
      <template #icon>
        <a
          class="proj-img"
          target="_blank"
          href="https://github.com/csc301-2023-fall/project-7-epoch-t"
          ><img class="thumbnail" src="../assets/images/epoch.jpg" alt=""
        /></a>
      </template>
      <template #heading>
        <a
          class="proj-title"
          target="_blank"
          href="https://github.com/csc301-2023-fall/project-7-epoch-t"
          >Epoch D&D Marketplace</a
        ></template
      >
      <template #description>
        An open-source Vue widget library offering reusable cross-platform Vue
        components for use by web developers of small to medium sized
        businesses, with PostgreSQL back-end architecture.
      </template>
      <template #stack>
        <img src="../assets/icons/icons8-postgres.svg" alt="postgres" />
        <img src="../assets/icons/icons8-javascript.svg" alt="javascript" />
        <img src="../assets/icons/icons8-vue.svg" alt="vue" />
      </template>
    </ProjectItem>
    <ProjectItem>
      <template #icon>
        <a
          class="proj-img"
          target="_blank"
          href="https://github.com/ATM-GSA/ATM"
          ><img class="thumbnail" src="../assets/images/atm.svg" alt=""
        /></a>
      </template>
      <template #heading>
        <a
          class="proj-title"
          target="_blank"
          href="https://github.com/ATM-GSA/ATM"
          >Application Tracking Manager</a
        ></template
      >
      <template #description>
        A centralized and authoritative resource for managing information about
        the Environment and Climate Change Canada Reusable Applications Division
        software applications.
      </template>
      <template #stack>
        <img src="../assets/icons/icons8-c-sharp-logo.svg" alt="csharp" />
        <img src="../assets/icons/icons8-dotnet.png" alt="dotnet" />
        <img src="../assets/icons/blazor.svg" alt="blazor" />
      </template>
    </ProjectItem>
    <ProjectItem>
      <template #icon>
        <a
          class="proj-img"
          target="_blank"
          href="https://github.com/roryhofland/personal-website"
          ><img class="thumbnail" src="../assets/images/github.svg" alt=""
        /></a>
      </template>
      <template #heading>
        <a
          class="proj-title"
          href="https://github.com/roryhofland/personal-website"
          target="_blank"
          >Personal Website v1.0</a
        ></template
      >
      <template #description>
        An old personal website I made, which was useful for learning web
        development without frontend frameworks such as Vue.
      </template>
      <template #stack>
        <img src="../assets/icons/icons8-javascript.svg" alt="javascript" />
      </template>
    </ProjectItem>
  </div>
</template>

<style>
i {
  margin: 10px 0 0 0;
  padding: 0;
}

img {
  width: 24px;
  padding: 0 2px;
  height: auto;
}

.thumbnail {
  width: 100%;
  height: 100%;
  border-radius: 10px;
}

.list-wrapper {
  display: grid;
}

.proj-title {
  color: white;
}

.proj-img:hover {
  filter: none;
}

@media (min-width: 1024px) {
  .list-wrapper {
    grid-template-columns: 50% 50%;
  }

  i {
    margin: 0;
  }
}
</style>
