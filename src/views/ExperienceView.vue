<template>
    <div>
        <HeaderMain />
        <PhotoSlider :items="photos"/>
        <ExperienceContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import PhotoSlider from '@/components/PhotoSlider.vue'
import ExperienceContent from '@/components/experiencePage/ExperienceContent.vue'
import photo1 from '../assets/experience/photo1.jpg'
import photo2 from '../assets/experience/photo2.jpg'
import photo3 from '../assets/experience/photo3.jpg'
import photo4 from '../assets/experience/photo4.jpg'
import photo5 from '../assets/experience/photo5.jpg'

export default {
    name: 'ExperiemceView',
    components: {
        HeaderMain,
        PhotoSlider, 
        ExperienceContent
    },
    setup(){
      const photos = [
        photo1, photo2, photo3, photo4, photo5
      ]

      return {photos}
    }
}
</script>
