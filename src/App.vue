<template> 
  <div :class="isDark ? '' : 'dark'">
    <div id="app" class="flex-1 bg-gray-600 dark:bg-white">
      <br>
      <div class="absolute ml-60 mt-12 transform lg:mt-14">
      <label for="toogleA" class="flex items-center cursor-pointer">
      <div class="relative">
        <input id="toogleA" type="checkbox" class="sr-only" @click="isDark =! isDark"/>
      <div class="w-10 h-4 bg-gray-400 rounded-full shadow-inner"></div>
      <div class="dot absolute w-6 h-6 bg-green-200 rounded-full shadow -left-1 -top-1 transition"></div>
      </div>
      </label>
      </div>
    
    <!-- Home page -->
    <p id="title" class="flex absolute text-white text-xl ml-7 mt-10 transition duration-500 ease-in-out hover:bg-green-600 text-grey-200 rounded-sm transform hover:-translate-y-1 hover:scale-110 dark:text-gray-900">Edomiyas &nbsp;<strong>Temesgen</strong></p>
    <button id="hamburger" class="flex text-green-200 text-3xl mt-10 lg:hidden" v-on:click="toggleNavbar()">
      <i class="fa fa-bars"></i>
    </button>
    <nav v-bind:class="{'hidden': !showMenu, 'flex': showMenu}" class="text-green-200 text-xl grid mt-12 lg:flex inline text-center space-x-14 -ml-20 md:ml-96">
      <NavLinks url="#" text="Home" class="ml-14 transition duration-500 ease-in-out hover:text-white rounded-sm transform hover:-translate-y-1 hover:scale-110 dark:text-gray-900" id="home"/>
      <NavLinks url="#br" text="About me" class="text-white transition duration-500 ease-in-out hover:text-green-200 rounded-sm transform hover:-translate-y-1 hover:scale-110 dark:text-gray-900"/>
      <NavLinks url="#ccc" text="CCC" class="text-white transition duration-500 ease-in-out hover:text-green-200 rounded-sm transform hover:-translate-y-1 hover:scale-110 dark:text-gray-900"/>
      <NavLinks url="#projects" text="Projects" class="text-white transition duration-500 ease-in-out hover:text-green-200 rounded-sm transform hover:-translate-y-1 hover:scale-110 dark:text-gray-900"/>
      <NavLinks url="#contact" text="Contact me" class="text-white transition duration-500 ease-in-out hover:text-green-200 rounded-sm transform hover:-translate-y-1 hover:scale-110 dark:text-gray-900"/>
    </nav>
    <div id="social-media" class="flex justify-end space-x-4 -mt-7 mr-10">
      <a href="https://www.linkedin.com/in/edomiyas-temesgen-16ba01173/" target="_blank"><img :src="image"  alt="linkedin" id="linkedin" class="hidden max-w-full w-7 lg:flex"></a>
      <p id="linkedintext" class="hidden text-white mt-1 lg:flex hover:text-blue-200 dark:text-gray-900">LinkedIn</p>
      <a href="https://github.com/etemesgen/" target="_blank"><img src="./assets/github.png" alt="github" id="github" class="hidden max-w-full w-7 lg:flex"></a>
      <p id="githubtext" class="hidden text-white mt-1 lg:flex hover:text-gray-200 dark:text-gray-900">GitHub</p>
    </div>
    <p id="dev" class="bg-green-200 w-56 p-1 font-bold text-xl text-center ml-20 rounded transition duration-500 ease-in-out hover:bg-yellow-200 text-grey-200 rounded-sm transform hover:-translate-y-1 hover:scale-110 lg:ml-36 w-60 mt-24 md:mt-36">Full-Stack Developer</p>
    <img class="flex w-10 ml-80 mt-14 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 lg:float-right mr-24 md:-mt-7" src="./assets/javascript.png" alt="javascript" id="javascript">
    <img class="flex w-40 -mt-10 ml-32 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 lg:w-48 md:float-right -mr-52" :src="me" alt="me" id="me">  <!-- Mobile first responsive, define mobile size by default -->
    <img class="flex w-20 ml-12 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/php.png" alt="php" id="php">
    <img class="flex w-32 ml-64 -mt-8 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/vue.png" alt="vue" id="vue">
    <br>
    <p id="quote" class="flex text-white text-xl font-bold ml-10 lg:text-3xl md:-mt-80 dark:text-gray-900">If you never failed,</p>
    <p id="quote2" class="flex text-white text-xl font-bold ml-24 lg:text-3xl dark:text-gray-900">you never tried anything new.</p>
    <p class="hidden lg:flex ml-36 mt-10 text-gray-400">I love creating interfaces, coding and pretty much learning new things.</p>
    <p class="text-center mt-10 text-xl text-green-200 hvr-underline-from-center lg:ml-36"><a href="#contact">LET'S CHAT !</a></p><br>
    <a href="#br"><img class="animate-bounce w-8 m-auto mt-10 lg:w-12" src="./assets/scroll.png" alt="scroll" id="scroll"></a>

    <!-- Second page -->

    <p class="text-3xl mt-24 text-center lg:hidden">👋🏽</p>
    <br id="br">
    <p class="text-xl text-center text-white md:text-3xl dark:text-gray-900" id="hello">Hello! &nbsp;I’m Edomiyas Temesgen</p>
    <p class="text-white text-center italic dark:text-gray-900" id="para1">“First, solve the problem. Then, write the code.” – John Johnson</p>
    <br>
    <p class="text-gray-400 text-center mt-10" id="para4">That’s what coding teaches me every day. 
      Before even thinking to code, we have to be a 
      problem solver. Being a third year software 
      engineering student with an internship, 
      i work to succeed using my passion for living.</p>

    <img class="absolute w-14" src="./assets/problem-solving.png" alt="problem solving" id="problem-solving">
    <img class="absolute w-9 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/right-arrow.png" alt="right-arrow" id="right-arrow">
    <img class="absolute" src="./assets/web-programming.png" alt="programming" id="programming">
  
    <div class="grid">
      <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid1">
        <p class="text-green-200 ml-4 mt-2" id="front">Front-End</p>
        <img class="w-10 ml-1 mt-2" src="./assets/html.png" alt="html" id="html">
        <img class="w-6 ml-14 -mt-9" src="./assets/CSS3.png" alt="css" id="css">
        <img class="w-9 -mt-8" src="./assets/tailwind.png" alt="tailwind" id="tailwind">
        <img class="w-7" src="./assets/javascript.png" alt="javascript" id="javascript2">
        <img src="./assets/vue.png" alt="vue" id="vue2">
        <img class="w-8" src="./assets/chartjs.png" alt="vue" id="chartjs">
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid2">
        <p class="text-green-200 ml-4 mt-2" id="back">Back-End</p>
        <img class="w-10 ml-4 mt-3" src="./assets/php.png" alt="php" id="php2">
        <img class="w-8 ml-24 -mt-7" src="./assets/python.png" alt="python" id="python">
        <img class="w-14 -mt-10 ml-40" src="./assets/java.png" alt="java" id="java">
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid3">
        <p class="text-green-200 ml-4 mt-2" id="db">Database</p>
        <img class="w-16 ml-4 mt-1" src="./assets/mysql.png" alt="mysql" id="mysql">
        <img class="w-12 -mt-12 ml-28" src="./assets/mongodb.png" alt="mongodb" id="mongodb">
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid4">
        <p class="text-green-200 ml-4 mt-2" id="devops">DevOps</p>
        <img class="w-10 mt-2 ml-6" src="./assets/docker.png" alt="docker" id="docker">
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid5">
        <p class="text-green-200 ml-4 mt-2" id="ui">UI/UX Design</p>
        <img class="w-7 ml-6 mt-3" src="./assets/figma.png" alt="figma" id="figma">
        <img class="w-9 -mt-8 ml-20" src="./assets/adobexd.png" alt="adobexd" id="adobexd">
      </div>
       <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid6">
        <p class="text-green-200 ml-4 mt-2" id="vs">Version Control</p>
        <img class="w-12 mt-1 ml-6" src="./assets/git.png" alt="git" id="git">
      </div>
       <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid7">
        <p class="text-green-200 ml-4 mt-2" id="mb">Mobile Developement</p>
        <img class="w-8 mt-2 ml-6" src="./assets/react-native.png" alt="react-native" id="react-native">
      </div>
      <div class="bg-gray-500 h-24 w-72 ml-16 mt-10 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110 dark:bg-gray-400" id="grid8">
        <p class="text-green-200 ml-4 mt-2" id="tools">Tools</p>
        <img class="w-7 ml-4 mt-3" src="./assets/visual.png" alt="visual" id="visual">
        <img class="w-7 ml-16 -mt-7" src="./assets/eclipse.png" alt="eclipse" id="eclipse">
        <img class="w-7 -mt-7 ml-28" src="./assets/github.png" alt="github2" id="github2">
        <img class="w-7 ml-40 -mt-7" src="./assets/wamp.png" alt="wamp" id="wamp">
        <img class="w-9 -mt-8 ml-52" src="./assets/postman.png" alt="postman" id="postman">
      </div>

    <!-- Third page -->

    <p id="ccc" class="text-center mt-36 text-3xl text-white transition duration-500 ease-in-out hover:bg-yellow-200 transform hover:-translate-y-1 dark:text-gray-900">CCC</p>
    <div id="curiosity">
      <h1 class="text-center text-2xl mt-20 hvr-underline-from-center" id="cu">Curiosity</h1>
      <p class="text-center text-xl text-white mt-5 dark:text-gray-900" id="cupara">is what got me into IT development.</p>
    </div>

    <div id="creativity">
      <h1 class="text-green-200 text-center text-2xl mt-20 hvr-underline-from-center" id="cr">Creativity</h1>
      <p class="text-center text-xl text-white mt-5 dark:text-gray-900" id="crpara">is what motivates me in my developer adventure.</p>
    </div>

    <div id="concept">
      <h1 class="text-blue-400 text-center text-2xl mt-20 hvr-underline-from-center" id="co">Concept</h1>
      <p class="text-center text-xl text-white mt-5 dark:text-gray-900" id="copara">is what fascinates me about IT development.</p>
    </div>

    <img class="mt-20 -ml-2 transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" id="graph" src="./assets/graph2.png" alt="graph">
    </div>
    
    <!-- Fourth page -->

    <p id="projects" class="text-center mt-36 text-3xl text-white transition duration-500 ease-in-out hover:bg-green-200 transform hover:-translate-y-1 dark:text-gray-900">Discover my projects</p>
    <div id="all-project">
      <div id="project1">
      <a href="https://time-display-edo.netlify.app/" target="_blank"><img class="mt-16 w-80 ml-12 rounded transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/timeDisplay.png" alt="timedisplay" id="timedisplay"></a>  
        <img class="w-14 ml-20 mt-10" src="./assets/html.png" alt="html" id="html2">
        <img class="w-9" src="./assets/CSS3.png" alt="css" id="css2">
        <img class="w-9 -mt-10" src="./assets/javascript.png" alt="javascript" id="javascript3">
      </div>
      <div id="project2">
      <a href="https://github.com/etemesgen/PPE_France_Montagnes_Dynamique" target="_blank"><img class="mt-16 w-80 ml-12 rounded transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/FranceMontagne.png" alt="francemontagne" id="francemontagne"></a>
        <img class="w-14 ml-20 mt-9" src="./assets/html.png" alt="html" id="html3">
        <img class="w-9" src="./assets/CSS3.png" alt="css" id="css3">
        <img class="w-12 -mt-10" src="./assets/php.png" alt="php" id="php3">
      </div>
      <div id="project3">
      <a href="https://github.com/etemesgen/PPE2_Gmail_single_page-back-end" target="_blank"><img class="mt-16 w-80 ml-12 rounded transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/gmail.jpg" alt="gmail" id="gmail"></a>
        <img class="w-14 ml-16 mt-9" src="./assets/html.png" alt="html" id="html4">
        <img class="w-9" src="./assets/CSS3.png" alt="css" id="css4">
        <img class="w-9 -mt-10" src="./assets/javascript.png" alt="javascript" id="javascript4">
        <img class="w-12 -mt-8" src="./assets/php.png" alt="php" id="php4">
      </div>
      <div id="project4">
       <a href="https://github.com/etemesgen/Interface_admin_gestion_client" target="_blank"><img class="mt-16 w-80 ml-12 rounded transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/Interfaceadmingestionclient.png" alt="interfaceadmin" id="interfaceadmin"></a>
        <img class="w-14 ml-16 mt-9" src="./assets/html.png" alt="html" id="html5">
        <img class="w-9" src="./assets/CSS3.png" alt="css" id="css5">
        <img class="w-12 -mt-9" src="./assets/php.png" alt="php" id="php5">
        <img class="w-16 -mt-10" src="./assets/mysql.png" alt="mysql" id="mysql2">
      </div>
      <div id="project5">
       <a href="https://github.com/etemesgen/personnel" target="_blank"><img class="mt-16 w-80 ml-12 rounded transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/GestionPersonnel.png" alt="gestionpersonnel" id="gestionpersonnel"></a>
        <img class="w-20 ml-44 mt-4" src="./assets/java.png" alt="java" id="java2">
      </div>
      <div id="project6">
        <a href="https://tip-calculator-app-edo.vercel.app/" target="_blank"><img class="mt-16 w-80 ml-12 rounded transition duration-500 ease-in-out hover: transform hover:-translate-y-1 hover:scale-110" src="./assets/tipcalculator.png" alt="tipcalculator" id="tipcalculator"></a>  
        <img class="w-14 ml-20 mt-10" src="./assets/html.png" alt="html" id="html6">
        <img class="w-9" src="./assets/CSS3.png" alt="css" id="css6">
        <img class="w-9 -mt-10" src="./assets/javascript.png" alt="javascript" id="javascript5">
      </div>
      <p class="ml-36 mt-20 text-xl text-green-200 hvr-underline-from-center" id="allprojects"><a href="https://github.com/etemesgen?tab=repositories" target="_blank">ALL PROJECTS</a></p>
    </div>

    <!-- Fifth page -->

    <p class="text-white mt-20 text-4xl dark:text-gray-900" id="contact">Start by <span class="hvr-underline-from-center text-green-200 -mt-3">saying hi</span></p>
    <br>
    <br>
    <form id="form" action="https://formsubmit.co/temesgen.edomiyas@yahoo.com" method="POST">
      <input class="focus:ring-2 focus:ring-green-200 bg-gray-500 text-white italic rounded ml-20 mt-10 w-64 h-9 dark:bg-gray-300" type="text" name="name" id="name" placeholder=" Your name" required>
      <br>
      <input class="focus:ring-2 focus:ring-green-200 bg-gray-500 text-white italic rounded ml-20 mt-5 w-64 h-9 dark:bg-gray-300" type="text" name="email" id="email" placeholder=" Your email" required>
      <br>
      <textarea class="focus:ring-2 focus:ring-green-200 bg-gray-500 text-white italic rounded ml-20 mt-5 w-64 h-40 dark:bg-gray-300" name="message" id="message" cols="30" rows="10" placeholder=" Your message..."></textarea>
      <br>
      <br>
      <button class="bg-green-200 text-xl w-36 h-9 text-green-500 rounded-sm transition duration-500 ease-in-out hover:bg-transparent rounded-sm transform hover:-translate-y-1 hover:scale-110" value="submit" id="button">Send ✅</button>
    </form>
    <p class="hidden text-gray-400" id="teme">E-mail</p>
    <p class="text-white text-xl ml-16 mt-2 hover:text-yellow-200 dark:text-gray-900" id="info">temesgen.edomiyas@yahoo.com</p>
      <NavLinks url="#" text="Home" class="hidden text-green-200 ml-14 transition duration-500 ease-in-out hover:bg-white-200 text-white rounded-sm transform hover:-translate-y-1 hover:scale-110" id="homenav"/>
      <NavLinks url="#br" text="About me" class="hidden text-green-200 ml-14 transition duration-500 ease-in-out hover:bg-white-200 text-white rounded-sm transform hover:-translate-y-1 hover:scale-110" id="aboutnav"/>
      <NavLinks url="#ccc" text="CCC" class="hidden text-green-200 ml-14 transition duration-500 ease-in-out hover:bg-white-200 text-white rounded-sm transform hover:-translate-y-1 hover:scale-110" id="cccnav"/>
      <NavLinks url="#projects" text="Projects" class="hidden text-green-200 ml-14 transition duration-500 ease-in-out hover:bg-white-200 text-white rounded-sm transform hover:-translate-y-1 hover:scale-110" id="projectnav"/>
      <NavLinks url="#contact" text="Contact me" class="hidden text-green-200 ml-14 transition duration-500 ease-in-out hover:bg-white-200 text-white rounded-sm transform hover:-translate-y-1 hover:scale-110" id="contactnav"/>
    <img class="w-28 mt-5" src="./assets/_EdoCode.png" alt="logo" id="logo">
    <a href="https://www.linkedin.com/in/edomiyas-temesgen-16ba01173/" target="_blank"><img :src="image"  alt="linkedin" id="linkedin2" class="max-w-full w-7 mt-4"></a>
    <a href="https://github.com/etemesgen/" target="_blank"><img src="./assets/github.png" alt="github" id="github3" class="max-w-full w-7 -mt-7"></a>
    <p class="text-gray-400 ml-16 mt-5 dark:text-gray-900" id="love">2021. Made with ❤ by ⚡ Edomiyas ⚡</p><br>
    <p id="title2" class="hidden text-white text-xl ml-7">Edomiyas &nbsp;<strong>Temesgen</strong></p>
    <a href="#title"><img class="animate-bounce ml-80 -mt-20" src="./assets/Arrow.png" alt="arrow" id="arrow"></a>
    <br>
    </div>
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
      showMenu: false,
      isDark: true
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
  background: #9FFAC9;
}

/* Toggle A */
input:checked ~ .dot {
  transform: translateX(100%);
  background-color: #FFFFFF;
}

#hamburger{
  margin-left: 22rem;
}

#javascript{
  margin-left: 20rem;
}

#css{
  margin-top: -2.37rem;
}

#tailwind{
  margin-left: 6rem;
}

#chartjs{
  margin-left: 15.5rem;
}

#javascript2{
  margin: -2.1rem 0rem 0rem 9.5rem;
}

#vue2{
  width: 2.1rem;
  margin: -1.9rem 0rem 0rem 12.5rem;
}

#chartjs{
  margin-top: -2rem;
}

#cu{
  color: #FBFF42;
}

#css2{
  margin: -3.4rem 0rem 0rem 12rem;
}

#javascript3{
  margin-left: 18.5rem;
}

#css3{
  margin: -3.4rem 0rem 0rem 12rem;
}

#php3{
  margin-left: 18rem;
}

#css4{
  margin: -3.4rem 0rem 0rem 9.5rem;
}

#javascript4{
  margin-left: 14.5rem;
}

#php4{
  margin-left: 19rem;
}

#css5{
  margin: -3.4rem 0rem 0rem 9.5rem;
}

#php5{
  margin-left: 14rem;
}

#mysql2{
  margin-left: 18.5rem;
}

#css6{
  margin: -3.4rem 0rem 0rem 12rem;
}

#javascript5{
  margin-left: 18rem;
}

#problem-solving{
  margin: -9.5rem 0rem 0rem 6rem;
}

#right-arrow{
  margin: -9rem 0rem 0rem 12rem;
}

#programming{
  width: 2.9rem;
  margin: -9.2rem 0rem 0rem 18rem;
}

#contact{
  margin-left: 4.5rem;
}

#button{
  margin-left: 8.5rem;
}

#logo{
  margin-left: 9.5rem;
}

#linkedin2{
  margin-left: 10.7rem;
}

#github3{
  margin-left: 13.7rem;
}

 @media only screen and (min-width: 1200px) {

    #title{
      margin-top: 2.9rem;
    }

    #me{
      position: absolute;
      margin-left: 70rem;
    }

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

    a::before{
      content: "";
      position: absolute;
      display: block;
      width: 100%;
      height: 2px;
      bottom: 0;
      left: 0;
      background-color: #9FFAC9;
      transform: scaleX(0);
      transition: transform 0.3s ease;
    }

    a:hover::before{
      transform: scaleX(1);
    }

    /* Underline From Center */
    .hvr-underline-from-center {
      display: inline-block;
      vertical-align: middle;
      -webkit-transform: perspective(.1rem) translateZ(0);
      transform: perspective(.1rem) translateZ(0);
      box-shadow: 0 0 .1rem rgba(0, 0, 0, 0);
      position: relative;
      overflow: hidden;
    }
    
    .hvr-underline-from-center:before {
      content: "";
      position: absolute;
      z-index: -1;
      left: 51%;
      right: 51%;
      bottom: 0;
      background: #9FFAC9;
      height: .2rem;
      -webkit-transition-property: left, right;
      transition-property: left, right;
      -webkit-transition-duration: 0.3s;
      transition-duration: 0.3s;
      -webkit-transition-timing-function: ease-out;
      transition-timing-function: ease-out;
    }
    .hvr-underline-from-center:hover:before,
    .hvr-underline-from-center:focus:before,
    .hvr-underline-from-center:active:before {
      left: 0;
      right: 0;
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
      margin: -11rem 0rem 0rem 7rem;
    }

    #html{
      width: 3.5rem;
      margin: .7rem 0rem 0rem 0.3rem;
    }
    
    #css{
      width: 2.2rem;
      margin: -3.3rem 0rem 0rem 5.2rem;
    }

    #tailwind{
      width: 2.8rem;
      margin: -3rem 0rem 0rem 9rem;
    }

    #javascript2{
      width: 2.5rem;
      margin: -2.5rem 0rem 0rem 13.5rem;
    }

    #vue2{
      width: 2.5rem;
      margin: -2.5rem 0rem 0rem 17.7rem;
    }

    #chartjs{
      width: 2.5rem;
      margin: -2.5rem 0rem 0rem 21.5rem;
    }

    #grid2{
      margin: -2rem 0rem 0rem 7rem;
    }

    #php2{
      width: 3.5rem;
      margin: 1rem 0rem 0rem 1rem;
    }

    #python{
      width: 2.8rem;
      margin: -2.4rem 0rem 0rem 7rem;
    }

    #java{
      width: 4.5rem;
      margin: -3.3rem 0rem 0rem 12rem;
    }

    #grid3{
      margin: 1rem 0rem 0rem 7rem;
    }

    #mysql{
      width: 4.5rem;
      margin: 0.5rem 0rem 0rem 1rem;
    }

    #mongodb{
      width: 3.5rem;
      margin: -3.5rem 0rem 0rem 9rem;
    }

    #grid4{
      margin: -8rem 0rem 0rem 34rem;
    }

    #docker{
      width: 3.5rem;
      margin: 0.5rem 0rem 0rem 1.5rem;
    }

    #grid5{
      margin: -8rem 0rem 0rem 61rem;
    }

    #figma{
      width: 2.3rem;
      margin: 1rem 0rem 0rem 1.5rem;
    }

    #adobexd{
      width: 2.7rem;
      margin: -2.5rem 0rem 0rem 6rem;
    }

    #grid6{
      margin: 1rem 0rem 0rem 7rem;
    }

    #git{
      width: 3.5rem;
      margin: 0.5rem 0rem 0rem 1.5rem;    
    }

    #grid7{
      margin: -8rem 0rem 0rem 34rem;
    }

    #react-native{
      width: 3rem;
      margin: 0.5rem 0rem 0rem 1.5rem; 
    }

    #grid8{
      margin: -8rem 0rem 0rem 61rem;
    }

    #visual{
      width: 2.3rem;
      margin: 1rem 0rem 0rem 1rem;
    }
    
    #eclipse{
      width: 2.3rem;
      margin: -2.3rem 0rem 0rem 5.5rem;
    }

    #github2{
      width: 2.4rem;
      margin: -2.5rem 0rem 0rem 10.5rem;
    }

    #wamp{
      width: 2.5rem;
      margin: -2.4rem 0rem 0rem 15.5rem;
    }

    #postman{
      width: 3rem;
      margin: -2.7rem 0rem 0rem 20.5rem;
    }

    #hello{
      display: flex;
      margin: 4rem 0rem 9rem 34rem;
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

    #cu, #cr, #co{
      margin: 5rem 0rem 0rem 7rem;
      text-align: left;
    }

    #cupara, #crpara, #copara{
      margin: 2rem 0rem 0rem 10rem;
      text-align: left;
    }

    #graph{
      width: 30rem;
      margin: -26rem 0rem 0rem 55rem;
    }

    #timedisplay{
      width: 28rem;
      margin-left: 2rem;
    }

    #html2{
      margin-left: 6rem;
    }

    #css2{
      margin-left: 15rem;
    }

    #javascript3{
      margin-left: 23rem;
    }

    #francemontagne{
      width: 29.5rem;
      margin: -19.2rem 0rem 0rem 32.8rem;
    }

    #html3{
      margin: 2.5rem 0rem 0rem 38rem;
    }

    #css3{
      margin: -3.4rem 0rem 0rem 47rem;
    }

    #php3{
      margin: -2.3rem 0rem 0rem 55rem;
    }

    #gmail{
      width: 28rem;
      margin: -18.7rem 0rem 0rem 65rem;
    }

    #html4{
      margin: 2.5rem 0rem 0rem 67rem;
    }

    #css4{
      margin: -3.4rem 0rem 0rem 75rem;
    }

    #javascript4{
      margin: -2.6rem 0rem 0rem 82rem;
    }

    #php4{
      margin: -2rem 0rem 0rem 88rem;
    }

    #interfaceadmin{
      width: 28rem;
      margin-left: 2rem;
    }

    #html5{
      margin: 2.5rem 0rem 0rem 4rem;
    }

    #css5{
      margin: -3.4rem 0rem 0rem 11rem;
    }

    #php5{
      margin: -2.4rem 0rem 0rem 17rem;
    }

    #mysql2{
      margin: -2.4rem 0rem 0rem 22.5rem;
    }

    #gestionpersonnel{
      width: 28rem;
      margin: -13.6rem 0rem 0rem 33rem;
    }

    #java2{
      margin: 1rem 0rem 0rem 45rem;
    }
    
    #tipcalculator{
      margin: -20.7rem 0rem 0rem 69rem;
    }

    #html6{
      margin-left: 70rem;
    }

    #css6{
      margin-left: 78rem;
    }

    #javascript5{
      margin-left: 86rem;
    }

    #allprojects{
      margin-left: 43rem;
    }

    #contact{
      margin: 9rem 0rem 0rem 10rem;
    }

    #name{
      width: 20rem;
      margin: 2rem 0rem 0rem 10rem;
      outline: none;
    }

    #email{
      width: 20rem;
      margin: 2rem 0rem 0rem 10rem;
      outline: none;
    }

    #message{
      width: 20rem;
      margin: 2rem 0rem 0rem 10rem;
      outline: none;
    }
  
    #button{
      margin-left: 15.5rem;
    }

    #arrow{
      margin: -3rem 0rem 0rem 80rem;
    }

    #teme{
      display: flex;
      position: absolute;
      font-size: 1.2rem;
      margin: -25rem 0rem 0rem 55rem;
    }

    #info{
      margin: -22rem 0rem 0rem 55rem;
      font-size: 1.5rem;
    }

    #logo{
      display: flex;
      position: absolute;
      width: 10rem;
      height: 9rem;
      margin: 3.3rem 0rem 0rem 65rem;
    }

    #love{
      margin: 25rem 0rem 0rem 30rem;
    }

    #title2{
      display: flex;
      margin: -3.2rem 0rem 0rem 10rem;
    }

    #linkedin2{
      position: absolute;
      margin: 24.5rem 0rem 0rem 55rem;
    }

    #github3{
      position: absolute;
      margin: 24.5rem 0rem 0rem 58.5rem;
    }

    #homenav, #aboutnav, #cccnav, #projectnav, #contactnav{
      display: flex;
      position: absolute;
    }

    #homenav{
      margin: 3rem 0rem 0rem 56rem;
    }

    #aboutnav{
      margin: 5rem 0rem 0rem 56rem;
    }

    #cccnav{
      margin: 7rem 0rem 0rem 56rem;
    }

    #projectnav{
      margin: 9rem 0rem 0rem 56rem;
    }

    #contactnav{
      margin: 11rem 0rem 0rem 56rem;
    }
  }
</style>
