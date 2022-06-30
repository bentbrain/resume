<script setup>
import JobVue from "./Job.vue";
</script>

<template>
  <div class="experience">
    <h2>Experience</h2>
    <JobVue :key="job" v-for="job in includedJobs" :job="job" />
  </div>
</template>

<script>
export default {
  name: "Experience",
  props: {
    jobs: Array,
  },
  computed: {
    // a computed getter
    includedJobs() {
      // `this` points to the component instance
      return this.jobs.filter((i) => i.include === true);
    },
  },
};
</script>
