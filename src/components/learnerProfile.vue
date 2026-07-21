<script setup>
defineProps({
  name: String,
  program: String,
  track: String,
  studentID: String
})
</script>

<template>
  <div>
    <h2>Learner Profile</h2>

    <p><strong>Learner Name:</strong> {{ name }}</p>
    <p><strong>Program:</strong> {{ program }}</p>
    <p><strong>Learning Track:</strong> {{ track }}</p>
    <p><strong>Student ID:</strong> {{ studentID }}</p>
  </div>
</template>