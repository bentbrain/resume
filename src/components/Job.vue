<script setup>
import SkillVue from "./Skill.vue";
</script>

<template>
  <div class="job">
    <div class="top">
      <div class="left">
        <h3>{{ job.position }}</h3>
        <p class="date">
          <strong>{{ job.company }}</strong
          >, {{ job.startDate }} – {{ job.endDate }}
        </p>
      </div>
      <img :src="`../src/assets/logos/${job.logo}`" alt="" />
    </div>

    <div class="text">
      <div class="description">
        <div class="skills">
          <SkillVue :key="skill" v-for="skill in job.skills" :skill="skill" />
        </div>
        <p :key="para" v-for="para in job.description">{{ para }}</p>
      </div>

      <div v-if="job.achievements[0]" class="achievements">
        <h4>Achievements:</h4>

        <p :key="para" v-for="para in job.achievements">{{ para }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Job",
  props: {
    job: Object,
  },
};
</script>
