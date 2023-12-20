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
      <button class="button is-ghost">Ghost</button>
    </footer>
  </section>
  <Objective :language="language" v-on:updateLanguage="updateLanguage" />
</template>

<script setup>
import { ref, getCurrentInstance } from 'vue';
import Objective from './components/Objective.vue'; 

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
