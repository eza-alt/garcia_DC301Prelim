<script setup>
defineProps({
  courses: Array
})
</script>

<template>
  <div>
    <h2>Course List</h2>

    <ul>
      <li
        v-for="course in courses"
        :key="course"
      >
        {{ course }}
      </li>
    </ul>
  </div>
</template>