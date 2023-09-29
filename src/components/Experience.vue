<script setup>
import { ref } from 'vue';

const professional = ref([
    {project:'Sample 01', duration:'2019-2020', Description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
    {project:'Sample 02', duration:'2019-2020', Description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
    {project:'Sample 03', duration:'2019-2020', Description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
    {project:'Sample 04', duration:'2019-2020', Description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
    {project:'Sample 05', duration:'2019-2020', Description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
])


const Volunteering = ref([
    {project:'LEO Club of Kuruwita/Paradise', duration:'01/2023-Present', Description: 'Top board member of LEO Club of Kuruwita/Pardise.'},
    {project:'Sri Lankan Girl Guide Association', duration:'2013-2019', Description: 'Member of Sri Lankan Girl Guide Association- 1stRathnapura Team - Ferguson High School, Rathnapura, Sri Lanka.'},
    {project:'School Eastern Music Orchestra ', duration:'2015-2017', Description: 'Member of School Eastern Music Orchestra and Signing Group.'},
])
</script>

<template>
    <h1>My Experience</h1>
    <div class="main">
        <div class="myExp" v-for="Exp in professional">
            <div class="topic">
                <h2>{{ Exp.project }}</h2>
                <h3>{{ Exp.duration }}</h3>
            </div>
            <p>{{ Exp.Description }}</p>
        </div>
    </div>

    <h1 class="vol">Volunteering</h1>
    <div class="main">
        <div class="myExp" v-for="Exp in Volunteering">
            <div class="topic">
                <h2>{{ Exp.project }}</h2>
                <h3>{{ Exp.duration }}</h3>
            </div>
            <p>{{ Exp.Description }}</p>
        </div>
    </div>
</template>


<style scoped>
h1 {
    margin-left: 20rem;
    margin-top: 5rem;
    line-height: 9rem;
}

.vol {
    text-align: right;
    margin-right: 20rem;
}

h2 {
    font-size: 200%;
    line-height: normal;
}

.main {
    padding-left: 10rem;
    padding-right: 10rem;
    place-items: center;
}

.myExp {
    display: grid;
    grid-template-columns: repeat(2, 2fr);
    grid-column-gap: 5rem;
    padding: 1rem;
}

.myExp .topic{
    text-align: right;
}
</style>