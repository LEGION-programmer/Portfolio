<template>
  <div class="container">
    <div class="logo">
      <h1 @click="home()">{{ headerLogo }}</h1>  
    </div>
    <div class="options">
      <a class="links" @click="experience()">Doświadczenie</a>
      <a class="links" @click="projects()">Projekty i technologie</a>
      <a class="links" @click="about()">O mnie</a>
      <a class="links" @click="media()">Media</a>
      <a class="links" @click="contact()">Kontakt</a>
    </div>
  </div>
</template>

<script>
import { useRouter } from 'vue-router'

export default {
  name: 'HeaderMain',

  data() {
    return {
      headerLogo: "<LEGION />",
      router: useRouter()
    }
  },

  methods: {
    about(){
      this.router.push({ name: 'about' })
    },

    home(){
      this.router.push({ name: 'home' })
    },

    experience(){
      this.router.push({ name: 'experience' })
    },

    projects(){
      this.router.push({ name: 'projects' })
    },

    media(){
      this.router.push({ name: 'media' })
    },
    
    contact(){
      this.router.push({ name: 'contact' })
    }
  }
}
</script>

<style lang="scss" scoped>
*{
  font-family: sans-serif;
}

.container{
  display: grid;
  grid-template-columns: 1fr 2fr;
  justify-content: center;
  background-color: #e8e8e8;
  box-shadow: 0 5px 1em #000000;
  border-radius: 30px;
}

.logo{
  justify-self: center;
  align-self: center;

  >h1{
    background: -webkit-linear-gradient(right, #072AC8, #3B322C);
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }
}

.options{
  justify-self: end;
  align-self: center;
  >.links{
    text-decoration: none;
    color: #3B322C;
    margin: 20px;
    font-size: 18px;
  }
}

a:hover{
    cursor: pointer;
}
</style>
