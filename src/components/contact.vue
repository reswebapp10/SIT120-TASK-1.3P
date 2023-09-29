<script setup>
import { ref } from 'vue';

defineProps({
    name: {
        type: String,
        required: true
    }
})

const Details = ref([
    {icon: 'https://pics.freeicons.io/uploads/icons/png/18070286501543238910-512.png', refer: '0412549053'},
    {icon: 'https://pics.freeicons.io/uploads/icons/png/11082093271551939477-512.png', refer: 'manumihenagamage@gmail.com'},
    {icon: 'https://pics.freeicons.io/uploads/icons/png/10999648851580817583-512.png', refer: '13 Flourish Drive, Mount Duneed, VIC3217'},
])
</script>


<template>
    <div class="main">
        <h1>Contact me</h1>
        <div class="Contact">
            <div class="details">
                <div class="organization" v-for="item in Details">
                <div class="description">
                    <img :src=item.icon alt="" width="10" height="auto">
                </div>
                <div class="refer">
                    <h2>{{ item.refer }}</h2>
                </div>
            </div>
            </div>


            <div class="myForm">
                <form>
                <h2>Name</h2>
                <input v-model="reservationContact" type="text" placeholder="Your Name">
                
                <h2>Email</h2>
                <input type="email" placeholder="Email">
                
                <h2>Contact Number</h2>
                <input v-model="reservationContact" type="tel" placeholder="Mobile Number">

                <h2>Message</h2>
                <input type="text" class="Message" placeholder="Your Message">
                <br>
                <button class="reserved" @click='addreservation' >Send Message</button>
                </form>
                </div>
        </div>
    </div>
</template>

<style scoped>

h1{
    padding-top: 3rem;
    line-height: 5rem;
    padding-bottom: 3rem;
    text-align: center;
}

.main {
    background-image: url('https://images.unsplash.com/photo-1584947113973-cb90c09ff5da?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    background-attachment: fixed;
    padding-bottom: 3rem;
}

.main .Contact{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-column-gap: 5rem;
}

.details {
    display: block;
    margin-left: 10rem;
    border-radius: 2rem;
    background-color: rgba(0, 0, 0, 0.655);
    place-items: center;
}

.refer h2{
    text-align: left;
}


.main .organization{
    position: relative;
    display: grid;
    grid-template-columns: repeat(2,1fr);
    grid-column-gap: 5rem;
    padding: 1rem;
    place-items: center;
}

.myForm{
    background-color: rgba(0, 0, 0, 0.655);
    padding: 3rem;
    place-items: center;
    border-radius: 2rem;
    text-align: center;
    margin-right: 10rem;
}

.main .organization  .description{
    text-align: right;
}



.myForm input{
    border: none;
    padding: 0.5rem;
    border-radius: 0.25rem;
    min-width: 10rem;
}

.myForm button{
    margin-top: 2rem;
    background-color: rgb(13, 253, 0);
    color: black;
    padding: 0.5rem;
    border-radius: 0.5rem;
    font-size: x-large;
    font-weight: 700;
}

.Message{
    min-height: 5rem;
}

.myForm button:hover{
    background-color: aqua;
    border-color: azure;
    transition: 0.5s;
}
</style>