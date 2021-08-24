<template> 
  <div id="app" class="flex-1">
    <p id="title" class="text-white mt-9 ml-8">Edomiyas <strong>Temesgen</strong></p>
    <nav class="-mt-7 ml-80 text-xl text-green-300 flex space-x-20">
      <NavLinks url="#" text="Home" class="hover:text-white"/>
      <NavLinks url="#" text="About me" class="hover:text-white"/>
      <NavLinks url="#" text="Projects" class="hover:text-white"/>
      <NavLinks url="#" text="Contact me" class="hover:text-white"/>
    </nav>
    <div id="social-media" class="flex justify-end space-x-4 -mt-7 mr-10">
      <a href="#"><img :src="image"  alt="linkedin" id="linkedin" class="max-w-full w-7"></a>
      <p id="linkedintext" class="text-white mt-1">LinkedIn</p>
      <a href="#"><img src="./assets/github.png" alt="github" id="github" class="max-w-full w-7"></a>
      <p id="githubtext" class="text-white mt-1">GitHub</p>
    </div>
  </div>
</template>

<script>
import NavLinks from './components/NavLinks.vue'
import image from "./assets/linkedin.png"

export default {
  name: 'App',
  components: {
    NavLinks
  },
  data(){
    return{
      image: image
    }
  }
}
</script>


<style>
@import url('http://fonts.cdnfonts.com/css/rockwell-nova');

body{
  font-family: 'Rockwell Nova';
}
</style>
