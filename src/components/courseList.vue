<script setup>
const courses = [
  "Programming",
  "Information Management",
  "JavaScript ",
  "Domain Course",
  "Database Management"
]

</script>

<template>
 
    <h2>Course List</h2>

    <ul>
      <li
        v-for="course in courses":key="course">
        {{ course }}
      </li>
    </ul>
 
</template>