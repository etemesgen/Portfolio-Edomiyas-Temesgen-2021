<template> 
  <div id="app" class="flex-1">
    <p id="title" class="text-white mt-9 ml-8">Edomiyas <strong>Temesgen</strong></p>
    <nav class="-mt-7 ml-80 text-xl text-green-300 flex space-x-20 md:">
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
    <p id="dev" class="bg-green-300 w-56 p-1 font-bold text-xl text-center mt-28 ml-36 rounded">Full-Stack Developer</p>
    <p class="text-white text-3xl ml-36 mt-7">If you never failed,</p>
    <p class="text-white text-3xl ml-72">you never tried anything new.</p>
    <img class="w-40 float-right mr-64 -mt-32" :src="me" alt="me">
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
      me: me
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
