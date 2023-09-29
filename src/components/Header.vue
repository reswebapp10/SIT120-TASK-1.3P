<script setup>
defineProps({
    name: {
        type: String,
        required: true
    }
})

</script>

<template>
    <div class="nav">
        <h1>{{ name }}</h1>
        <div class="links">
            <a href="#">Contact</a>
            <a href="#">Skills</a>
            <a href="#">Experience</a>
        </div>
    </div>
</template>

<style scopeed>
.nav{
    display: flex;
    min-height: 10vh;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    min-width: 100%;
    place-items: center;
    float: inline-start;
    background-color: rgba(10, 10, 10, 0.512);
}

.nav h1{
    color: rgb(255, 255, 255);
    font-size: 2rem;
    font-weight: 800;
}

.links{
    display: flex;
    text-align: left;
    font-size: larger;
}

.links a{
    text-decoration: none;
    padding: 1.2rem;
    color: rgb(255, 255, 255);
    font-weight: 700;
}

.links a:hover{
    color: rgb(0, 0, 0);
    background-color: rgb(43, 255, 0);
    border-radius: 1rem;
    transition: 0.4s;
    scale: 1.2;
}
</style>