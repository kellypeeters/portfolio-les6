<script setup>
import { RouterLink, RouterView } from 'vue-router'
import  StartpaginaComp from './components/StartpaginaComp.vue'
import  SitetitleComp from './components/SitetitleComp.vue'
import  WerkenComp from './components/WerkenComp.vue'
import NavComp from './components/NavComp.vue'
import  FooterComp from './components/FooterComp.vue'
import { ref } from 'vue';

/*const x = ref(0)

function onMousemove(e) {
  x.value = e.clientX
}
*/
</script> 

<template>
  <div>
<div class="
    w-screen h-screen 
    bg-regular-orange
    dark:bg-regular-gray
    text-regular-lightorange dark:text-gray-400
    animate-fade animate-once 
    ">
      <NavComp />
      <StartpaginaComp />
  </div>
      <div class="
        w-full h-full
        bg-regular-orange
        dark:bg-regular-gray
        text-regular-lightorange dark:text-gray-400
        animate-fade animate-once
        ">
        <SitetitleComp />
      </div>
      <div class="
        w-full h-full
        bg-white
        text-regular-lightorange 
        animate-fade animate-once
        ">
        <WerkenComp />
      </div>
      <div class="
        bg-regular-orange
        dark:bg-regular-gray
        text-regular-lightorange dark:text-gray-400
        animate-fade animate-once 
        ">
        <FooterComp /> 
      </div>
    </div>
</template>

<style>
.movearea {
  transition: 0.3s background-color ease;
}


/*
  https://router.vuejs.org/guide/advanced/transitions.html
  https://vuejs.org/guide/built-ins/transition.html

  Enter and leave animations can use different
  durations and timing functions.
*/
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}
.slide-fade-leave-active {
  transition: all 0.1s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(1vh);
  opacity: 0;
}
</style>

