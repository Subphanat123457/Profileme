<template>
  <section style="background-color: rgb(248, 163, 35);" class="hero is-link  has-text-centered">
    <div class="image-container">
      <img class="p-center" src="./image/Screenshot 2023-12-21 162807.png" width="100px" alt="">
    </div>  
    <div class="hero-body">
      <p class="title">
        SUPANAT WIBOONPANIT
      </p>
      <p class="subtitle">
        Software Developer
      </p>
      <p class="">
        Hello there! I'm Supanut Wiboonpanich and Nickname Aom, a Computer Science student at Maejo University, Class of 27.
      </p>
      
    </div>
    <footer>
      <button class="button is-ghost text-color" @click="toggleLanguage">Language {{ language }}</button>
    </footer>
    
  </section>
  <Objective :language="language" v-on:updateLanguage="updateLanguage" />
  <Certificate :language="language" v-on:updateLanguage="updateLanguage" />
  <Skill :language="language" v-on:updateLanguage="updateLanguage" />
  <Education :language="language" v-on:updateLanguage="updateLanguage" />
  <Activities :language="language" v-on:updateLanguage="updateLanguage" />
  <Footer />

</template>

<script setup>
import { ref, getCurrentInstance } from 'vue';
import Objective from './components/Objective.vue'; 
import Certificate from './components/certificate.vue';
import Skill from './components/Skill.vue';
import Education from './components/Education.vue';
import Activities from './components/Activities.vue';
import Footer from './components/Footer.vue';

let language = ref('en');
const { emit } = getCurrentInstance();

const toggleLanguage = () => {
  language.value = language.value === 'en' ? 'th' : 'en';
  console.log(language.value);
  emit('updateLanguage', language.value);
};

const updateLanguage = (newLanguage) => {
  language.value = newLanguage;
};



</script>

<style scoped>
@media print {
  @page {
    size: A4; /* Change to your desired size */
    margin: 0; /* Adjust margins as needed */
  }
  body {
    transform: scale(0.75); /* Adjust scale as needed */
    transform-origin: top left;
  }

  /* Hide elements you don't want to print */
  .navbar, .footer, .button {
    display: none;
  }

  /* Adjust the size and layout of elements as needed */
  .hero, .hero-body, .title, .subtitle {
    width: 100%;
    page-break-inside: avoid;
  }
}
.p-center{
  margin-top: 1rem;
}
.text-color {
  color: #000000;
}
.image-container {
  display: flex;
  justify-content: center;
}

</style>
