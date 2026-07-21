<script setup>
import {ref, computed} from 'vue'

const learnerName = ref("Jeneza Garcia")
const Program = ref("BSIT")
const learnerTrack =ref("Information Technology")
const studentId = ref(18549)



const increase = value++

const decrease = value--

const logo =" https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQPp1qolkZBcGtKzvi-WyupaYNT_c9zDMiFGLM4rcLnzA&s=10"

const mycourses = ref([
  'Information Technology',
  'Networking',
  'Doamin Course',
  'Programming',
  'Web System Development'
])

const courses = computed(() => courses.value.length)



const status = true


const learnerprofile = defineProps({
name: String,
program: String,
track: String,
studentId: Number

 
})


const courselist = defineProps({


 
})



</script>
<template>
      <h1> Online Course Enrollment System</h1>

<h3>Completed Lessons</h3>
  <button @click="increase">complete</button>
  <button @click="decrease">undo</button>


 <img :src="logo" width="150">

<p v-if = status >in Progress</p>
<p v-else>Completed</p>


  
</template>

