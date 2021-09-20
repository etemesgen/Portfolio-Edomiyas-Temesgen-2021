<template> 
  <div id="app" class="flex-1">
    <p id="title" class="flex absolute text-white text-xl ml-7">Edomiyas &nbsp;<strong>Temesgen</strong></p>
    <button id="hamburger" class="flex text-green-200 text-3xl ml-80 mt-10 lg:hidden" v-on:click="toggleNavbar()">
      <i class="fa fa-bars"></i>
    </button>
    <nav v-bind:class="{'hidden': !showMenu, 'flex': showMenu}" class="text-green-200 text-xl grid mt-12 lg:flex inline text-center space-x-14 -ml-20 md:ml-96">
      <NavLinks url="#" text="Home" class="ml-14 hover:text-white"/>
      <NavLinks url="#hello" text="About me" class="hover:text-white"/>
      <NavLinks url="#" text="CCC" class="hover:text-white"/>
      <NavLinks url="#" text="Projects" class="hover:text-white"/>
      <NavLinks url="#" text="Contact me" class="hover:text-white"/>
    </nav>
    <div id="social-media" class="flex justify-end space-x-4 -mt-7 mr-10">
      <a href="#"><img :src="image"  alt="linkedin" id="linkedin" class="hidden max-w-full w-7 lg:flex"></a>
      <p id="linkedintext" class="hidden text-white mt-1 lg:flex">LinkedIn</p>
      <a href="#"><img src="./assets/github.png" alt="github" id="github" class="hidden max-w-full w-7 lg:flex"></a>
      <p id="githubtext" class="hidden text-white mt-1 lg:flex">GitHub</p>
    </div>
    <p id="dev" class="bg-green-200 w-56 p-1 font-bold text-xl text-center ml-16 rounded lg:ml-36 w-60 mt-24 md:mt-36">Full-Stack Developer</p>
    <img class="flex w-10 ml-72 mt-14 lg:float-right mr-24 md:-mt-7" src="./assets/javascript.png" alt="javascript">
    <img class="flex w-40 -mt-10 ml-24 lg:w-48 md:float-right -mr-52" :src="me" alt="me">  <!-- Mobile first responsive, define mobile size by default -->
    <img class="flex w-20 ml-7" src="./assets/php.png" alt="php" id="php">
    <img class="flex w-32 ml-56 -mt-8" src="./assets/vue.png" alt="vue" id="vue">
    <br>
    <p id="quote" class="flex text-white text-xl font-bold ml-3 lg:text-3xl md:-mt-80">If you never failed,</p>
    <p id="quote2" class="flex text-white text-xl font-bold ml-20 lg:text-3xl">you never tried anything new.</p>
    <p class="hidden lg:flex ml-36 mt-10 text-gray-300">I love creating interfaces, coding and pretty much learning new things.</p>
    <a href=""><p id="contact" class="text-center mt-10 text-xl text-green-200 underline lg:flex md:ml-36">LET'S CHAT !</p></a>
    <a href="#hello"><img class="w-8 m-auto mt-10 lg:w-12" src="./assets/scroll.png" alt="scroll" id="scroll"></a>


    <p class="text-3xl mt-24 text-center lg:hidden">👋🏽</p>
    <br>
    <p class="text-xl text-center text-white md:text-3xl" id="hello">Hello! &nbsp;I’m Edomiyas Temesgen</p>
    <p class="text-white text-center italic" id="para1">“First, solve the problem. Then, write the code.” – John Johnson</p>
    <br>
    <p class="text-gray-300 text-center mt-10" id="para4">That’s what coding teaches me every day. 
      Before even thinking to code, we have to be a 
      problem solver. Being a third year software 
      engineering student with an internship, 
      i work to succeed using my passion for living.</p>

    <img class="absolute w-14 -mt-48 ml-20" src="./assets/problem-solving.png" alt="problem solving" id="problem-solving">
    <img class="absolute w-9 -mt-44 ml-40" src="./assets/right-arrow.png" alt="right-arrow" id="right-arrow">
    <img class="absolute w-14 -mt-48 ml-60" src="./assets/web-programming.png" alt="programming" id="programming">

    <div class="grid">
      <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid1">
        <p class="text-green-200 ml-4 mt-2" id="front">Front-End</p>
        <img class="w-10 ml-3 mt-2" src="./assets/html.png" alt="html" id="html">
        <img class="w-6 ml-16 -mt-9" src="./assets/CSS3.png" alt="css" id="css">
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid2">
        <p class="text-green-200 ml-4 mt-2" id="back">Back-End</p>
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid3">
        <p class="text-green-200 ml-4 mt-2" id="db">Database</p>
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid4">
        <p class="text-green-200 ml-4 mt-2" id="devops">DevOps</p>
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid5">
        <p class="text-green-200 ml-4 mt-2" id="ui">UI/UX Design</p>
      </div>
       <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid6">
        <p class="text-green-200 ml-4 mt-2" id="vs">Version Control</p>
      </div>
       <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid7">
        <p class="text-green-200 ml-4 mt-2" id="mb">Mobile Developement</p>
      </div>
       <div class="bg-gray-500 h-24 w-72 ml-10 mt-10" id="grid8">
        <p class="text-green-200 ml-4 mt-2" id="tools">Tools</p>
      </div>
    </div>
    <br>
    <br>
    <br>

  </div>
</template>

<script>
import NavLinks from './components/NavLinks.vue'
import image from "./assets/linkedin.png"
import me from "./assets/me.png"

export default {
  name: 'App',
  components: {
    NavLinks
  },
  data(){
    return{
      image: image,
      me: me,
      showMenu: false
    }
  },
  methods: {
    toggleNavbar: function(){
      this.showMenu = !this.showMenu;
    }
  }
}
</script>


<style>
@import url('http://fonts.cdnfonts.com/css/rockwell-nova');

html{
  scroll-behavior: smooth;
}

body{
  font-family: 'Rockwell Nova', sans-serif;
}

#css{
  margin-top: -2.37rem;
}

 @media only screen and (min-width: 1500px) {
    #php{
      display: flex;
      width: 6rem;
      margin: 9rem 0rem 0rem 61rem;
    }

    #vue{
      display: flex;
      width: 9rem;
      margin: 0rem 0rem 0rem 82rem;
    }

    #scroll{
      margin: auto;
      margin-top: 7rem;
    }

    #quote{
      margin-left: 9rem;
    }

    #quote2{
      margin-left: 15rem;
    }

    #grid1, #grid2, #grid3, #grid4, #grid5, #grid6, #grid7, #grid8{
      height: 8rem;
      width: 25rem;
    }

    #front, #back, #db, #devops, #ui, #vs, #mb, #tools{
      margin: 1rem 0rem 0rem 1.5rem;
      font-size: 1.1rem;
    }

    #grid1{
      margin: -12rem 0rem 0rem 7rem;
    }

    #html{
      width: 3.5rem;
      margin: .7rem 0rem 0rem 1rem;
    }
    
    #css{
      width: 2.2rem;
      margin: -3.3rem 0rem 0rem 5.5rem;
    }

    #grid2{
      margin: -2rem 0rem 0rem 7rem;
    }

    #grid3{
      margin: 2rem 0rem 0rem 7rem;
    }

    #grid4{
      margin: -8rem 0rem 0rem 34rem;
    }

    #grid5{
      margin: -8rem 0rem 0rem 61rem;
    }

    #grid6{
      margin: 2rem 0rem 0rem 7rem;
    }

    #grid7{
      margin: -8rem 0rem 0rem 34rem;
    }

    #grid8{
      margin: -8rem 0rem 0rem 61rem;
    }

    #hello{
      display: flex;
      margin: 12rem 0rem 9rem 34rem;
    }
  
    #para1{
      display: flex;
      font-size: 1.5rem;
      margin: -8rem 0rem 0rem 34rem;
    }

    #para4{
      display: flex;
      margin: 0rem 0rem 0rem 32rem;
      text-align: center;
    }

    #problem-solving{
      display: flex;
      width: 3.5rem;
      position: absolute;
      margin: 1.5rem 0rem 0rem 52rem;
    }

    #right-arrow{
      display: flex;
      width: 2.3rem;
      position: absolute;
      margin: 2.5rem 0rem 0rem 58rem;
    }

    #programming{
      display: flex;
      width: 3rem;
      position: absolute;
      margin: 2.1rem 0rem 0rem 63.7rem;
    }
  }
</style>
