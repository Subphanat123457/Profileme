<template>
  <section style="background-color: rgb(248, 163, 35);" class="hero is-link has-text-centered">
    <div class="hero-body">
      <p class="title">
        SUPANAT WIBOONPANIT
      </p>
      <p class="subtitle">
        Software Developer
      </p>
    </div>
    <footer>
      <button class="button is-ghost text-color" @click="toggleLanguage">Language {{ language }}</button>
    </footer>
  </section>
  <Objective :language="language" v-on:updateLanguage="updateLanguage" />
  <Certificate :language="language" v-on:updateLanguage="updateLanguage" />
  <Skill :language="language" v-on:updateLanguage="updateLanguage" />

</template>

<script setup>
import { ref, getCurrentInstance } from 'vue';
import Objective from './components/Objective.vue'; 
import Certificate from './components/Certificate.vue';
import Skill from './components/Skill.vue';

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
.text-color {
  color: #000000;
}


</style>
