<script setup>
import { ref } from 'vue';

const Education = ref([
    {org: 'Deakin University, Waurn Ponds, VIC', Duration: '07/2023 – Current', Description: 'Bachelor of Information Technology'},
    {org: 'Universal College Lanka', Duration: '01/2022 - 10/2022 – Current', Description: 'Monash University Foundation Year (MUFY), Achievements: 4HD / 4D (Average 82.5%)'},
    {org: 'Ferguson High School, Rathnapura, Sri Lanka', Duration: '04/2021 – 08/2021', Description: 'Graduated from high school'},
])
</script>

<template>
    <div class="main">
        <div class="Edu">
            <h1>Education</h1>
            <div class="organization" v-for="myEdu in Education">
                <div class="description">
                    <h2>{{ myEdu.org }}</h2>
                    <h3>{{ myEdu.Duration }}</h3>
                </div>
                <div>
                    <p>{{ myEdu.Description }}</p>
                </div>
            </div>
        </div>
        
        <div class="image"></div>
    </div>
</template>


<style scoped>

h1{
    margin-left: 20rem;
    line-height: 5rem;
    padding-bottom: 3rem;
}

.main {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 10rem;
    grid-column-gap: 5rem;
}

.main .organization{
    position: relative;
    display: grid;
    grid-template-columns: repeat(2,1fr);
    grid-column-gap: 5rem;
    padding: 1rem;
}

.main .image {
    background-color: aqua;
    background-image: url('https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2072&q=80');
    background-size: cover;
    background-position: center;
    min-width: 10rem;
    min-height: 10vh;
    border-radius: 1rem;
}

.main .organization  .description{
    text-align: right;
}
</style>