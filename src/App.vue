<template> 
  <div id="app">
    <p id="title">Edomiyas <strong>Temesgen</strong></p>
    <nav>
      <NavLinks url="#" text="Home"/>
      <NavLinks url="#" text="About me"/>
      <NavLinks url="#" text="Projects"/>
      <NavLinks url="#" text="Contact me"/>
    </nav>
    <div id="social-media">
      <a href="#"><img :src="image"  alt="linkedin" id="linkedin"></a>
      <p id="linkedintext">LinkedIn</p>
      <a href="#"><img src="./assets/github.png" alt="github" id="github"></a>
      <p id="githubtext">GitHub</p>
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
/*@import url('http://fonts.cdnfonts.com/css/rockwell-nova');*/

body{
  background-color: #4E5A6B;
  margin: 0;
  padding: 0;
  font-family: 'Rockwell Nova';
}

#app {
  display: flex;
}

#title{
  margin: 2em 0rem 0rem 5rem;
  font-size: 1.2rem;
  color: #FFFFFF;
}

nav {
  margin: 2.3rem 0rem 0rem 6rem;
  font-size: 1.2rem;
}

nav a{
  text-decoration: none;
  color: #9FFAC9;
  margin-left: 4rem;
}

nav a:hover{
  color: #FFFFFF;
}

#linkedin{
  max-width: 100%;
  width: 1.7rem;
  margin: 2.2rem 0rem 0rem 7rem;
  background-color: #4E5A6B;
}

#linkedintext{
  margin: -1.8rem 0rem 0rem 9.2rem;
  color: #FFFFFF;
}

#github{
  max-width: 100%;
  width: 1.7rem;
  margin: -2rem 0rem .8rem 16rem;
  background-color: #4E5A6B;
}

#githubtext{
  margin: -2.6rem 0rem 0rem 18.5rem;
  color: #FFFFFF;
}
</style>
