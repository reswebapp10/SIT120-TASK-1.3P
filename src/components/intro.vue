<script setup>
defineProps({
    name: {
        type: String,
        required: true
    }
})
</script>

<template>
    <div class="intro">
        <div class="photo">
        </div>
        <div class="text">
            <h1>{{ name }}</h1>
            <p>Highly motivated, skilled individual seeking a position in a renowned 
                organization, with a passion for excellence, eager to deliver top-tier 
                client service through talent and commitment.
            </p>

            <button class="Contact">Contact Me</button>

        </div>
    </div>
</template>

<style scoped>
.intro{
    min-width: 100%;
    background-color: #181818;
    background-image: url("https://images.unsplash.com/photo-1604869515882-4d10fa4b0492?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    padding-top: 3rem;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    min-height: 90vh;
    padding-right: calc(var(--section-gap) / 2);
    padding-left: calc(var(--section-gap) / 2);
    place-items: center;
    background-attachment: fixed;
}

.intro .photo{
    background-image:url("./Images/01.png");
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    min-height: 85vh;
    min-width: 50rem;
}

.intro .text{
    background-color: rgba(0, 0, 0, 0.877);
    margin-left: -15rem;
    place-items: center;
    text-align: center;
    border-radius: 3rem;
    padding: 3rem;
    margin-right: 5rem;
}
.intro .text h1{
    text-align: center;
    font-size: 650%;
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-weight: 800;
    line-height: 5rem;
    color: aqua;
}

.intro .text p{
    font-size: 150%;
    text-align: justify;
    padding-top: 4rem;
}

.intro .text .Contact{
    background-color: rgb(13, 253, 0);
    color: black;
    padding: 1.5rem;
    border-radius: 1.5rem;
    font-size: x-large;
    font-weight: 700;
}

.intro .text .Contact:hover{
    background-color: aqua;
    border-color: azure;
    transition: 0.5s;
}
</style>