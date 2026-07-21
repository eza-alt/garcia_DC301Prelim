<script setup>
import { ref } from 'vue'

import learnerProfile from './components/LearnerProfile.vue'
import courseList from './components/CourseList.vue'

import courseImage from './assets/online-course.jpg'

const learner = {
  name: "Jeneza Garcia",
  program: "BS Information Technology",
  track: "Web Development",
  studentID: "2024-00001",
  status: true
}

const completedLessons = ref(0)

const courses = [
  "HTML Fundamentals",
  "CSS Essentials",
  "JavaScript Basics",
  "Vue.js 3",
  "Database Management"
]

function completeLesson() {
  completedLessons.value++
}

function undoLesson() {
  if (completedLessons.value > 0) {
    completedLessons.value--
  }
}
</script>

<template>
  <h1>Online Course Enrollment System</h1>

  <LearnerProfile
    :name="learner.name"
    :program="learner.program"
    :track="learner.track"
    :studentID="learner.studentID"
  />

  <h2>Completed Lessons: {{ completedLessons }}</h2>

  <button @click="completeLesson">Complete</button>
  <button @click="undoLesson">Undo</button>

  <br><br>

  <img
    :src="courseImage"
    width="350"
  />

  <CourseList
    :courses="courses"
  />

  <h3>
    Course Status:
    <span :style="{ color: learner.status ? 'green' : 'red' }">
      {{ learner.status ? 'In Progress' : 'Completed' }}
    </span>
  </h3>

  <h3>
    Learner Level:
    {{ courses.length >= 5 ? 'Advanced Learner' : 'Beginner Learner' }}
  </h3>
</template>