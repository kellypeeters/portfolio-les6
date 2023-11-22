<template>
  <div class="centered">
    <img src="src/assets/images/logo-grijs.png" alt="Logo" class="w-96 mb-5">

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
  
    <div class="
        text-5xl md:text-8xl lg:text-10xl 
        font-extrabold 
        h-screen font-titel
    ">
        <span class="typed-text">{{ typeValue }}</span>
        <span class="blinking-cursor">|</span>
        <span class="cursor" :class="{ typing: typeStatus }">&nbsp;</span>
    </div>
  </template>
  
  
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style lang="scss" scoped>
  
  // Cursor blinking CSS Starts...

  .centered {
  position: fixed;
  top: 50%;
  left: 50%;
  /* bring your own prefixes */
  transform: translate(-50%, -50%);
}
  .typed-text{
    color: white;
  }
  .blinking-cursor {
    color: #c9c9c9;
    -webkit-animation: 1s blink step-end infinite;
    -moz-animation: 1s blink step-end infinite;
    -ms-animation: 1s blink step-end infinite;
    -o-animation: 1s blink step-end infinite;
    animation: 1s blink step-end infinite;
  }
 
  @keyframes blink {
    from,
    to {
      color: transparent;
    }
    50% {
      color: #c9c9c9;
    }
  }
  @-moz-keyframes blink {
    from,
    to {
      color: transparent;
    }
    50% {
      color: #c9c9c9;
    }
  }
  @-webkit-keyframes blink {
    from,
    to {
      color: transparent;
    }
    50% {
      color: #c9c9c9;
    }
  }
  @-ms-keyframes blink {
    from,
    to {
      color: transparent;
    }
    50% {
      color: #c9c9c9;
    }
  }
  @-o-keyframes blink {
    from,
    to {
      color: transparent;
    }
    50% {
      color: #c9c9c9;
    }
  }
  // Cursor blinking CSS Ends...
  </style>
  