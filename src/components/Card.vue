<script setup>
import {defineProps} from 'vue'

const {quiz} = defineProps(['quiz'])


</script>

<template>
    <div class="card">
        <img :src="quiz.img" alt="">
        <div class="card-text">
          <h2>{{ quiz.name }}</h2>
          <p>{{ quiz.questions.length }} questions</p>
        </div>
      </div>
</template>

<style scoped>

@font-face {
  font-family: 'Oswald';
  src: url('../assets/Oswald.ttf');
}
@font-face {
  font-family: 'Edu';
  src: url('../assets/EduNSWACT.ttf');
}

.card {
  width: 310px;
  overflow: hidden;
  border-radius: 2%;
  box-shadow: 1px 1px 10px gray;
  margin-bottom: 35px;
  margin-right: 20px;
  cursor: pointer;
}

.card img {
  width: 100%;
  height: 180px;
  margin: 0;
}

.card .card-text {
  padding: 0;
}

.card .card-text h2 {
  font-family: 'Oswald';
  font-weight: bold;
  padding-left: 10px;
}
.card .card-text p {
  font-family: 'Edu';
  padding-left: 10px;
}
</style>
