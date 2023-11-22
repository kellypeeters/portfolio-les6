<template>
  <div class="
    w-screen h-screen  
    bg-regular-orange
    dark:bg-regular-gray
    text-regular-lightorange dark:text-gray-400
    animate-fade animate-once
    " id="werkervaring">

  <div class="logo-startpagina">
  <div class="bg-Pic dark:bg-Pic-dark w-96 h-96 mb-5"></div>
  </div>  
  <div class="centered">


  <div class="flex flex-col sm:flex-row sm:space-x-8 text-center">
    <div class="flex-auto text-regular-gray dark:text-regular-orange font-bold">
      Grafisch ontwerp
    </div>
    <div class="flex-none mt-2 invisible sm:visible">
      <svg xmlns="http://www.w3.org/2000/svg" 
        height="0.4em" 
        fill="white"
        viewBox="0 0 512 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
        <path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512z"/></svg>
    </div>
    <div class="flex-auto text-white font-bold">
      Datavisualisatie
    </div>
    <div class="flex-none mt-2 invisible sm:visible">
      <svg xmlns="http://www.w3.org/2000/svg" 
        height="0.4em" 
        fill="white"
        viewBox="0 0 512 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
        <path d="M256 512A256 256 0 1 0 256 0a256 256 0 1 0 0 512z"/></svg>
    </div>
    <div class="flex-auto text-regular-gray dark:text-regular-orange font-bold">
      Webdesign
    </div>
  </div>
</div>
</div>
  </template>
  
  <style> 
    .centered {
      width: 50%;
      margin: auto;
    }

    .dark .dark\:bg-Pic-dark {
      background-image: url("./src/assets/images/logo-grijs.png");
      background-size: 100% 100%;
    }
  
    .bg-Pic {
      background-image: url("./src/assets/images/logo-oranje.png");
      background-size: 100% 100%;
      display: block;
      margin: 0 auto; 
    }
 </style>
  