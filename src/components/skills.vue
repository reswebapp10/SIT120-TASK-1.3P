<script setup>
import { ref } from 'vue';

const mySkills = ref([
    {skill: "HTML", percentage:85},
    {skill: "CSS", percentage:75},
    {skill: "Vue3", percentage:95},
    {skill: "Python", percentage:80},
    {skill: "C++", percentage:85},
    {skill: "Java Script", percentage:95},
    {skill: "Java", percentage:90},
    {skill: "React", percentage:95}
])
</script>

<template>
    <div class="main">
        <h1>My Skills</h1>
        <div class="skills">
            <div class="myskills" v-for="mySkill in mySkills">
              <div class="skill">
                <div class="details">
                    <span>{{ mySkill.skill }}</span>
                    <span>{{ mySkill.percentage }}%</span>
                </div>
              <div class="bar">
                <div :style="{width: mySkill.percentage+'%'}"></div>
              </div>
            </div>
        </div>
    </div>
</div>
</template>

<style scoped>
.main {
    display: block;
    padding: 1.5rem;
    
}

.main h1 {
    margin-left: 20rem;
    font-size: xxx-large;
    color: aliceblue;
    font-weight: 800;
    margin-bottom: 3rem;
}
.skills {
    margin-left: 10%;
    padding-right: 5%;
    display: grid;
    grid-template-columns: repeat(2, 3fr);
    grid-column-gap: 7rem;
}



main .skill {
    padding: 0.75rem;
    display: block;
    margin-left: 10px;
    margin-bottom: 15px;
}

main .skill span{
    font-size: large;
}

main .details {
  width: 100%;
  display: flex;
  justify-content: space-between;
}

main .bar {
  margin-top: 10px;
  position: relative;
  background-color: lightgray;
  border-radius: 10px;
}

main .bar div {
  position: relative;
  height: 15px;
  width: 0;
  background-color: aqua;
  border-radius: 10px;
}


</style>