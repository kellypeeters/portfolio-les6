<template>
    <div class="
    w-full h-full  
    bg-fixed
    bg-regular-gray
    dark:bg-regular-orange
    text-regular-lightorange dark:text-gray-400
    animate-fade animate-once
    " id="werkervaring">

    <div class="
        text-xl md:text-xl lg:text-3xl 
        font-extrabold 
        font-titel
        pt-10 pl-10 mb-5
    ">
        <span class="typed-text">{{ typeValue }}</span>
        <span class="blinking-cursor">|</span>
        <span class="cursor" :class="{ typing: typeStatus }">&nbsp;</span>
    </div>

    <p class="text-4xl font-extrabold font-sans pb-5 mb-5
        animate-fade animate-delay-100 animate-ease-linear
        text-white p-10 mb-5
        ">WERKERVARING</p> 

        <div class="timeline">
  <ul>
    <li>
      <div class="right_content animate-fade-right animate-once animate-duration-[1500ms] animate-ease-in-out">
        <h1 class="text-regular-orange dark:text-regular-gray font-bold">Bpost</h1> 
        <p class="text-regular-lightgray">Jobstudent koerier</p>
      </div>
      <div class="left_content">
        <h3 class="font-titel">2023</h3>
      </div>
    </li>
    <li>
      <div class="right_content animate-fade-left animate-once animate-duration-[1500ms] animate-ease-in-out will-change-scroll">
        <h1 class="text-regular-orange dark:text-regular-gray font-bold">Ter heyden</h1>
        <p class="text-regular-lightgray">Jobstudent bar</p>
      </div>
      <div class="left_content">
        <h3 class="font-titel">2023</h3>
      </div>
    </li>
    <li>
      <div class="right_content animate-fade-right animate-once animate-duration-[1500ms] animate-ease-in-out will-change-scroll">
        <h1 class="text-regular-orange dark:text-regular-gray font-bold">BDO Belgium</h1>
        <p class="text-regular-lightgray">Stage grafisch ontwerp</p>
      </div>
      <div class="left_content">
        <h3 class="font-titel">2021</h3>
      </div>
    </li>
    <li>
      <div class="right_content animate-fade-left animate-once animate-duration-[1500ms] animate-ease-in-out">
        <h1 class="text-regular-orange dark:text-regular-gray font-bold">BDO Belgium</h1>
        <p class="text-regular-lightgray">Jobstudent digital marketeer</p>
      </div>
      <div class="left_content">
        <h3 class="font-titel">2020</h3>
      </div>
    </li>
    <li>
      <div class="right_content animate-fade-right animate-once animate-duration-[1500ms] animate-ease-in-out">
        <h1 class="text-regular-orange dark:text-regular-gray font-bold">WZC Armonea Eyckenborch</h1>
        <p class="text-regular-lightgray">Jobstudent keukenhulp en zaalmedewerker</p>
      </div> 
      <div class="left_content">
        <h3 class="font-titel">2016</h3>
      </div>
    </li> 
    <div style="clear:both;"></div>
  </ul>
</div>
    </div> 
</template> 
<script>
  export default {
    name: "typeWiriter",
    data: () => {
      return {
        typeValue: "",
        typeStatus: false,
        displayTextArray: ["Hallo,", 
        "Ik ben Kelly Peeters", 
        "Ik ben student grafisch ontwerp",
        "en dit is mijn werkervaring"],
        typingSpeed: 80,
        erasingSpeed: 80,
        newTextDelay: 2000,
        displayTextArrayIndex: 0,
        charIndex: 0,
      };
    },
    props: {},
    created() {
      setTimeout(this.typeText, this.newTextDelay + 200);
    },
    methods: {
      typeText() {
        if (this.charIndex < this.displayTextArray[this.displayTextArrayIndex].length) {
          if (!this.typeStatus) this.typeStatus = true;
          this.typeValue += this.displayTextArray[this.displayTextArrayIndex].charAt(
            this.charIndex
          );
          this.charIndex += 1;
          setTimeout(this.typeText, this.typingSpeed);
        } else {
          this.typeStatus = false;
          setTimeout(this.eraseText, this.newTextDelay);
        }
      },
      eraseText() {
        if (this.charIndex > 0) {
          if (!this.typeStatus) this.typeStatus = true;
          this.typeValue = this.displayTextArray[this.displayTextArrayIndex].substring(
            0,
            this.charIndex - 1
          );
          this.charIndex -= 1;
          setTimeout(this.eraseText, this.erasingSpeed);
        } else {
          this.typeStatus = false;
          this.displayTextArrayIndex += 1;
          if (this.displayTextArrayIndex >= this.displayTextArray.length)
            this.displayTextArrayIndex = 0;
          setTimeout(this.typeText, this.typingSpeed + 1000);
        }
      },
    },
  };
  </script>

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

/***********
* Timeline *
************/  
.timeline:before {
  content: '';
  position:absolute;
  height:85%;
  left:50%;
  width:2px;
  top:0px;
  background:#CECBCB;
  z-index:1;
}

.timeline{
  position:relative;
  margin: 50px auto;
  width:1000px;
  padding:0px 0px 90px 0px;
  top: -10px;
}

.timeline ul{
  margin:0;
  padding:0;
}

.timeline ul li{
  list-style:none;
  box-sizing:border-box; 
  line-height:normal;
  position:relative;
  width:50%;
  padding: 40px 30px;
}

.timeline ul li .right_content h1{
  padding:0px 2px 18px 0px;
}
.timeline ul li:nth-child(odd){
  float:left;
  text-align:right;
  clear:both;  
}

.timeline ul li:nth-child(even){
  float:right;
  text-align:left;
  clear:both;
}

.left_content{
  padding-bottom:20px;
}

.timeline ul li:nth-child(odd):before{
  content: '';
  position:absolute;
  width:10px;
  height:10px;
  background:#fff;
  border-radius:50%;
  right:-6px;
  top:44px;
  z-index:1;
}

.timeline ul li:nth-child(even):before{
  content: '';
  position:absolute;
  width:10px;
  height:10px;
  background:#fff;
  border-radius:50%;
  left:-4px;
  top:44px;
  z-index: 5;
}

.timeline ul li:nth-child(odd) .left_content{
  position:absolute;
  top:32px;
  right:-90px;
  margin:0;
  padding:8px 16px;

  color:#fff;
  border-radius:18px;
}

.timeline ul li:nth-child(even) .left_content{
  position:absolute;
  top:32px;
  left:-90px;
  margin:0;
  padding:8px 16px;
  
  color:#fff;
  border-radius:18px;
  
}


@media (max-width: 1000px){
  
  .timeline{
    width:100%;
  }
}

@media (max-width: 767px){
  .timeline{
    width:100%;    
    left:20px;
    top: -20px;
    padding-top: 40px;
    padding-bottom: 50px;
  }
  .timeline:before{
    left:20px;
  }
  .timeline ul li:nth-child(odd),
  .timeline ul li:nth-child(even){
    width:100%;
    text-align:left;
    padding-left:50px;
    padding-top: 10px;
    padding-bottom: 70px;
  }
  
  .timeline ul li:nth-child(odd):before
    {
    top:-18px;
    left:16px;
  
  }
  .timeline ul li:nth-child(even):before
  { 
    top:-18px;
    left:16px;
  }
  
    .timeline ul li:nth-child(odd) .left_content,
  .timeline ul li:nth-child(even) .left_content
  {
    top:-20px;
    left:50px;
    right:inherit;
    padding: 0px 2px 8px 0px;
  }

  .timeline ul li .right_content h1{
    padding: 2px 2px 8px 0px;
  }

  .timeline ul li .right_content p{
    padding: 0px 2px 8px 0px;
  }
}
</style>