<template>
  <div class="container">
    <div class="logo">
      <h1>{{ headerLogo }}</h1>  
    </div>
    <div class="options">
      <a href="#" class="links">Doświadczenie</a>
      <a href="#" class="links">Projekty i technologie</a>
      <a href="#" class="links">O mnie</a>
      <a href="#" class="links">Media</a>
      <a href="#" class="links">Kontakt</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderMain',

  setup() {
    const headerLogo = "<LEGION />"

    return {headerLogo}
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
</style>
