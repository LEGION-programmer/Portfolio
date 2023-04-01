<template>
  <div class="container">
    <div class="header">
      <div class="logo">
        <img src="../assets/LegionLogo.png" alt="Legion logo">
      </div>
      <div class="options">
        <img src="../assets/menu.png" alt="menu">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderMain'
}
</script>

<style scoped>
.container{
  display: grid;
  grid-template-columns: 130vh;
  justify-content: center;
  align-content: center;
  justify-items: stretch;
  align-items: center;
}

.header{
  display: grid;
  height: 100px;
  grid-template-columns: 1fr 50px;
  justify-content: center;
  align-content: center;
  align-items: center;
  justify-items: stretch;
  background-color: #e8e8e8;
  box-shadow: 0 5px 1em #000000;
  border-radius: 30px;
}

.logo>img{
  width: 80%;
  height: 100px;
}

.options>img{
  width: 40%;
  height: 40px;
  justify-self: end;
}
</style>
