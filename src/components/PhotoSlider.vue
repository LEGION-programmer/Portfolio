<template>
    <div class="photos">
        <img :src=items[0] alt="zpue" class="photo1">
        <img :src=items[1] alt="complex" class="photo2">
        <img :src=items[2] alt="factory" class="photo3">
        <img :src=items[3] alt="robot" class="photo4">
        <img :src=items[4] alt="robots" class="photo5">
    </div>
</template>
<script>
export default {
    name: 'PhotoSlider',
    props: ['items'],

}
</script>
<style lang="scss" scoped>
*{
  font-family: sans-serif;
}
.photos{
  margin-top: 30px;
  margin-bottom: 80px;
  display: grid;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-areas: 
  "photo1 photo2 photo3 photo4 photo5"
  ;
}
.photos>img{
  width: 70%;
  object-fit: cover;
  aspect-ratio: 1/1;
  border-radius: 100px;
  border: 1px solid #FCF300;
  box-shadow: 0 5px 1em #000000;
  &.photo1{
    position: relative;
    top: 40px;
    justify-self: center;
    grid-area: photo1;
    opacity: 0.4;
    animation: photo1-Slide 30s infinite;
  }
  &.photo2{
    position: relative;
    justify-self: center;
    top: 20px;
    grid-area: photo2;
    opacity: 0.7;
    animation: photo2-Slide 30s infinite;
  }
  &.photo3{
    position: relative;
    justify-self: center;
    grid-area: photo3;
    animation: photo3-Slide 30s infinite;
  }
  &.photo4{
    position: relative;
    top: 20px;
    justify-self: center;
    grid-area: photo4;
    opacity: 0.7;
    animation: photo4-Slide 30s infinite;
  }
  &.photo5{
    position: relative;
    top: 40px;
    justify-self: center;
    grid-area: photo5;
    opacity: 0.4;
    animation: photo5-Slide 30s infinite;
  }
}
@keyframes photo5-Slide {
0%, 14%{
  grid-area: photo5;
  opacity: 0.4;
  top: 40px;
}
15%, 18%{
  opacity: 0;
  top: 20px;
}
20%, 34%{
  grid-area: photo4;
  opacity: 0.7;
  top: 20px;
}
35%, 38%{
  opacity: 0;
  top: -20px;
}
40%, 54%{
  grid-area: photo3;
  opacity: 1;
  top: 0;
}
55%, 58%{
  opacity: 0;
  top: -20px;
}
60%, 74%{
  grid-area: photo2;
  opacity: 0.7;
  top: 20px;
}
75%, 78%{
  opacity: 0;
  top: 0;
}
80%, 94%{
  grid-area: photo1;
  opacity: 0.4;
  top: 40px;
}
95%, 98%{
  opacity: 0;
  top: 20px;
}
}
@keyframes photo4-Slide {
0%, 14%{
  grid-area: photo4;
  opacity: 0.7;
  top: 20px;
}
15%, 18%{
  opacity: 0;
  top: -20px;
}
20%, 34%{
  grid-area: photo3;
  opacity: 1;
  top: 0;
}
35%, 38%{
  opacity: 0;
  top: -20px;
}
40%, 54%{
  grid-area: photo2;
  opacity: 0.7;
  top: 20px;
}
55%, 58%{
  opacity: 0;
  top: 0;
}
60%, 74%{
  grid-area: photo1;
  opacity: 0.4;
  top: 40px;
}
75%, 78%{
  opacity: 0;
  top: 20px;
}
80%, 94%{
  grid-area: photo5;
  opacity: 0.4;
  top: 40px;
}
95%, 98%{
  opacity: 0;
  top: -20px;
}
}
@keyframes photo3-Slide {
0%, 14%{
  grid-area: photo3;
  opacity: 1;
  top: 0;
}
15%, 18%{
  opacity: 0;
  top: -20px;
}
20%, 34%{
  grid-area: photo2;
  opacity: 0.7;
  top: 20px;
}
35%, 38%{
  opacity: 0;
  top: 0;
}
40%, 54%{
  grid-area: photo1;
  opacity: 0.4;
  top: 40px;
}
55%, 58%{
  opacity: 0;
  top: 20px;
}
60%, 74%{
  grid-area: photo5;
  opacity: 0.4;
  top: 40px;
}
75%, 78%{
  opacity: 0;
  top: -20px;
}
80%, 94%{
  grid-area: photo4;
  opacity: 0.7;
  top: 20px;
}
95%, 98%{
  opacity: 0;
  top: -20px;
}
}
@keyframes photo2-Slide {
0%, 14%{
  grid-area: photo2;
  opacity: 0.7;
  top: 20px;
}
15%, 18%{
  opacity: 0;
  top: 0;
}
20%, 34%{
  grid-area: photo1;
  opacity: 0.4;
  top: 40px;
}
35%, 38%{
  opacity: 0;
  top: 20px;
}
40%, 54%{
  grid-area: photo5;
  opacity: 0.4;
  top: 40px;
}
55%, 58%{
  opacity: 0;
  top: -20px;
}
60%, 74%{
  grid-area: photo4;
  opacity: 0.7;
  top: 20px;
}
75%, 78%{
  opacity: 0;
  top: -20px;
}
80%, 94%{
  grid-area: photo3;
  opacity: 1;
  top: 0;
}
95%, 98%{
  opacity: 0;
  top: -20px;
}
}
@keyframes photo1-Slide {
0%, 14%{
  grid-area: photo1;
  opacity: 0.4;
  top: 40px;
}
15%, 18%{
  opacity: 0;
  top: 20px;
}
20%, 34%{
  grid-area: photo5;
  opacity: 0.4;
  top: 40px;
}
35%, 38%{
  opacity: 0;
  top: -20px;
}
40%, 54%{
  grid-area: photo4;
  opacity: 0.7;
  top: 20px;
}
55%, 58%{
  opacity: 0;
  top: -20px;
}
60%, 74%{
  grid-area: photo3;
  opacity: 1;
  top: 0;
}
75%, 78%{
  opacity: 0;
  top: -20px;
}
80%, 94%{
  grid-area: photo2;
  opacity: 0.7;
  top: 20px;
}
95%, 98%{
  opacity: 0;
  top: 0;
}
}
</style>