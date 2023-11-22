<script setup>
</script>


<template>
<!-- drawer init and toggle -->
<div class="text-right">
   <button 
    class="overflow-y-auto font-medium px-5 py-2.5 mr-2 mb-2" 
    type="button" 
    data-drawer-target="drawer-example" 
    data-drawer-show="drawer-example" 
    data-drawer-placement="top" 
    aria-controls="drawer-example"
    data-drawer-backdrop="false">
    <svg 
      xmlns="http://www.w3.org/2000/svg" 
      fill="white"
      height="1.3em" 
      viewBox="0 0 448 512">
      <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
      <path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg>
   </button>
</div>

 
 <!-- drawer component -->
 <div id="drawer-example" class="fixed top-0 left-0 z-40 h-screen w-screen p-4 overflow-y-auto transition-transform -translate-x-full
 bg-regular-gray w-80 
  " tabindex="-1" aria-labelledby="drawer-label">
    <button 
    type="button" 
    data-drawer-hide="drawer-example" 
    aria-controls="drawer-example" 
    class="text-gray-400 bg-transparent hover:text-white text-sm w-8 h-8 absolute top-2.5 right-2.5 inline-flex items-center justify-center dark:text-gray-400 dark:hover:text-white" >
       <svg class="w-3 h-3" 
       aria-hidden="true" 
       xmlns="http://www.w3.org/2000/svg" 
       fill="none" 
       viewBox="0 0 14 14">
          <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"/>
       </svg>
       <span class="sr-only">Close menu</span>
    </button>
    <img src="./src/assets/images/logo-grijs.png" alt="Logo" width="7%">
    <li class="font-bold pt-5 text-white text-center text-4xl font-titel">
      <ul class="p-10 mb-5 hover:text-regular-orange"><RouterLink to="/">HOME</RouterLink></ul>
      <ul class="p-10 mb-5 hover:text-regular-orange"><RouterLink to="/before">WERKERVARING</RouterLink></ul>
      <ul class="p-10 mb-5 hover:text-regular-orange"><RouterLink to="/new">PORTFOLIO</RouterLink></ul>
   </li>
   </div> 
</template>
 