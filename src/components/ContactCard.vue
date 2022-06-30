<template>
  <div class="contact-card">
    <img src="../assets/headshot.jpeg" alt="" />
    <h1>{{ contact[0].name }}</h1>
    <div class="info-block">
      <div
        class="contact-info"
        :key="type"
        v-for="(contact, type) in contact[0].details"
      >
        <p class="strong">{{ type }}:</p>
        <p>{{ contact }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactCard",
  props: {
    contact: Array,
  },
};
</script>
