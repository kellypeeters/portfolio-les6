<template>
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
  