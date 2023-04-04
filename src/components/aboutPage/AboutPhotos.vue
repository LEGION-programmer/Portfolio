<template>
    <div class="photos">
      <img src="../../assets/about/photo1.jpg" alt="gym" class="photo1">
      <img src="../../assets/about/photo2.jpg" alt="bike" class="photo2">
      <img src="../../assets/about/photo3.jpg" alt="code" class="photo3">
      <img src="../../assets/about/photo4.jpg" alt="football" class="photo4">
      <img src="../../assets/about/photo5.jpg" alt="motocycle" class="photo5">
    </div>
</template>

<script>
export default {
    name: 'AboutPhotos'
}
</script>

<style lang="scss" scoped>
*{
  font-family: sans-serif;
}
.photos{
  margin: 20px;
  display: grid;
  height: 350px;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-areas: 
  "photo1 photo2 photo3 photo4 photo5"
  ;
}

.photos>img{
  width: 70%;
  height: 180px;
  border-radius: 100px;
  border: 1px solid #FCF300;
  box-shadow: 0 5px 1em #000000;

  &.photo1{
    position: relative;
    top: 40px;
    justify-self: center;
    grid-area: photo1;
    opacity: 0.4;
  }

  &.photo2{
    position: relative;
    justify-self: center;
    top: 20px;
    grid-area: photo2;
    opacity: 0.7;
  }

  &.photo3{
    position: relative;
    justify-self: center;
    grid-area: photo3;
  }

  &.photo4{
    position: relative;
    top: 20px;
    justify-self: center;
    grid-area: photo4;
    opacity: 0.7;
  }

  &.photo5{
    position: relative;
    top: 40px;
    justify-self: center;
    grid-area: photo5;
    opacity: 0.4;
  }
}
</style>