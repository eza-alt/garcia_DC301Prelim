<script setup>
import { ref } from 'vue'

import learnerProfile from './components/learnerProfile.vue'
import courseList from './components/courseList.vue'

import courseImage from './assets/online-course.jpg'

const learner = {
  name: "Jeneza Garcia",
  program: "BS Information Technology",
  track: "Web Development",
  studentID: "18549",
  status: true
}

const completedLessons = ref(0)

const courses = [
  "Programming",
  "Information Management",
  "JavaScript ",
  "Domain Course",
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

const image =ref("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQvgultlCxhNVYkN-aM36JMZB44FI-vblwCAGsbzTkJNQ&s=10")
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


  
  <CourseList
  :courses="courses"/>

   <img :src="image">
  
</template>