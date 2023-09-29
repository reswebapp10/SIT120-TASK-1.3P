<script setup>
import Header from './components/Header.vue'
import intro from './components/intro.vue'
import skills from './components/skills.vue'
import Experience from './components/Experience.vue';
import Education from './components/Education.vue';
import contact from './components/contact.vue';

const name = "Manumi Henagamage"

</script>

<template>
  <div>
    <Header :name="name"/>
  </div>
  <header>
    <intro :name="name"/> 
  </header>
  <main>
    <skills />
    <Experience/>
    <Education/>
    <contact :name="name"/>
  </main>

  <footer>
    <p>{{ name }}. All rights reserved</p>
  </footer>
  
</template>


<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    place-items: center;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

footer{
  padding: 2rem;
  text-align: center;
  place-items: center;
}
</style>
