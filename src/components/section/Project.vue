<script setup>
import Card from "../Card.vue";
import {projectList} from "../../assets/data/projects"
</script>

<template>
  <section id="project">
    <div class="main">
      <h2>PROJECT & WORKSHOP</h2>
      <div class="project-list">
        <Card v-for="item in projectList" :key="item.title" :item="item" />
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  @apply min-h-[500px] bg-zinc-900 px-4 pb-20;
  .main {
    @apply container mx-auto text-zinc-100 max-w-[1220px] py-12;
    h2 {
      @apply text-2xl md:text-4xl font-semibold mb-12 sm:mb-16;
    }
    .project-list {
      @apply grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 md:gap-10;
    }
  }
}
</style>