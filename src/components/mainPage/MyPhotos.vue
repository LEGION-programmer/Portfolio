<template>
    <div class="photos">
      <img src="../../assets/home/myPhoto3.jpg" alt="Legion photo" class="photo1" ref="el">
      <img src="../../assets/home/myPhoto1.jpg" alt="Legion photo" class="photo2">
      <img src="../../assets/home/myPhoto2.jpg" alt="Legion photo" class="photo3">

      <div class="description">       
          <span class="typed-1">Mam na imię Tomek, jestem początkującym </span>
          <span class="typed-2">programistą i dziele się tutaj swoimi pracami, </span>
          <span class="typed-3">projektami, doświadczeniem oraz moimi</span>
          <span class="typed-4">różnymi przemyśleniami na ich temat.</span>        
      </div>
    </div>
</template>

<script>
export default {
  name: 'MyPhotos',

}
</script>

<style lang="scss" scoped>
*{
  font-family: sans-serif;
}

.photos{
  margin: 20px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas: 
  "photo1 photo2 photo3"
  ". description ."
  ;
}

.photos>img{
  width: 60%;
  object-fit: cover;
  aspect-ratio: 1/1;
  border-radius: 200px;
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
  margin-top: 60px;
  display: grid;
  grid-area: description;
  height: 100px;
  grid-template-columns: 1fr;
  justify-self: center;
  align-self: start;

  >span{
    display: block;
    text-align: center;
    font-weight: bolder;
    font-size: 16px;
    color: #3B322C;
    overflow: hidden;
    white-space: nowrap;
    width: 0;
  }
}

.typed-1{
  animation: typing 1.5s forwards;
  animation-delay: 1s;
}

.typed-2{
  animation: typing 1.5s forwards;
  animation-delay: 2.5s;
}

.typed-3{
  animation: typing 1.5s forwards;
  animation-delay: 4s;
}

.typed-4{
  animation: typing 1.5s forwards;
  animation-delay: 5.5s;
}

@keyframes typing {
  0%{
    border: 0;
  }
  1%{
    border-right: 2px solid;
  }
  99%{
    border-right: 2px solid;
  }
  100%{
    width: 100%;
  }
}

@media screen and (max-width: 1160px){
  .photos{
    grid-template-areas: 
    "photo1 photo2 photo3"
    "description description description"
    ;
  }
}
</style>