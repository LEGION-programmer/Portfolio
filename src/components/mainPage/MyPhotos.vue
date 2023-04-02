<template>
    <div class="photos">
      <img src="../../assets/myPhoto3.jpg" alt="Legion photo" class="photo1">
      <img src="../../assets/myPhoto1.jpg" alt="Legion photo" class="photo2">
      <img src="../../assets/myPhoto2.jpg" alt="Legion photo" class="photo3">

      <div class="description">
        <p>
          Mam na imię Tomek, jestem początkującym programistą i dziele się tutaj 
          swoimi pracami, doświadczeniem oraz różnymi przemyśleniami na ich temat.
        </p>
      </div>
    </div>
</template>

<script>
export default {
    name: 'MyPhotos'
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
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 250px 250px 250px;
  grid-template-areas: 
  "photo1 photo2 photo3"
  ". description ."
  ;
}

.photos>img{
  width: 50%;
  height: 200px;
  border-radius: 100px;
  border: 1px solid #FCF300;
  box-shadow: 0 5px 1em #000000;

  &.photo1{
    position: relative;
    top: 30px;
    justify-self: end;
    grid-area: photo1;
  }

  &.photo2{
    justify-self: center;
    grid-area: photo2;
  }

  &.photo3{
    position: relative;
    top: 30px;
    justify-self: start;
    grid-area: photo3;
  }
}

.description{
  grid-area: description;
  justify-self: center;
  align-self: start;

  >p{
    text-align: center;
    font-size: 18px;
    color: #3B322C;
  }
}
</style>