<template>
    <div>
        <HeaderMain />
        <PhotoSlider :items="photos"/>
        <AboutContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import PhotoSlider from '@/components/PhotoSlider.vue'
import AboutContent from '@/components/aboutPage/AboutContent.vue'
import photo1 from '../assets/about/photo1.jpg'
import photo2 from '../assets/about/photo2.jpg'
import photo3 from '../assets/about/photo3.jpg'
import photo4 from '../assets/about/photo4.jpg'
import photo5 from '../assets/about/photo5.jpg'

export default {
    name: 'AboutView',
    components: {
        HeaderMain,
        PhotoSlider,
        AboutContent
    },
    setup(){
      const photos = [
        photo1, photo2, photo3, photo4, photo5
      ]

      return {photos}
    }
}
</script>
