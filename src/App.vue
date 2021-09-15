<template> 
  <div id="app" class="flex-1">
    <p id="title" class="text-white text-xl mt-9 ml-4">Edomiyas <strong>Temesgen</strong></p>
    <button id="hamburger" class="flex text-green-200 text-3xl ml-64 -mt-7 lg:hidden" v-on:click="toggleNavbar()">
      <i class="fa fa-bars"></i>
    </button>
    <nav v-bind:class="{'hidden': !showMenu, 'flex': showMenu}" class="text-green-200 text-xl flex-col lg:inline text-center space-x-14 md:ml-96 -mt-10">
      <NavLinks url="#" text="Home" class="-ml-16 mt-12 hover:text-white"/>
      <NavLinks url="#" text="About me" class="hover:text-white"/>
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
    <p id="dev" class="bg-green-200 w-56 p-1 font-bold text-xl text-center ml-10 mt-24 rounded lg:ml-36">Full-Stack Developer</p>
    <img class="flex w-40 mr-36 mt-14 lg:w-48 float-right md:-mt-10" :src="me" alt="me">  <!--Mobile first responsive, define mobile size by default-->
    <br>
    <p class="text-white text-xl font-bold mt-64 lg:text-3xl">If you never failed,</p>
    <p class="flex text-white text-xl font-bold lg:text-3xl ml-72">you never tried anything new.</p>
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

body{
  font-family: 'Rockwell Nova', sans-serif;
}
</style>
