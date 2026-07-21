<script setup>

const props = defineProps({
  name: String,
  program: String,
  track: String,
  studentID: String
})
</script>

<template>
  <div>
    <h2>Learner Profile</h2>

    <p>Learner Name: {{ name }}</p>
    <p>Program:{{ program }}</p>
    <p>Learning Track: {{ track }}</p>
    <p>Student ID: {{ studentID }}</p>
  </div>
</template>