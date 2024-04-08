<template>
    <div>
        <HeaderMain />
        <PhotoSlider :items="photos"/>
        <MediaContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import PhotoSlider from '../components/PhotoSlider.vue'
import MediaContent from '../components/mediaPage/MediaContent.vue'
import photo1 from '../assets/media/photo1.jpg'
import photo2 from '../assets/media/photo2.jpg'
import photo3 from '../assets/media/photo3.jpg'
import photo4 from '../assets/media/photo4.jpg'
import photo5 from '../assets/media/photo5.jpg'

export default {
    name: 'MediaView',
    components: {
        HeaderMain,
        PhotoSlider,
        MediaContent
    },
    setup(){
      const photos = [
        photo1, photo2, photo3, photo4, photo5
      ]

      return {photos}
    }
}
</script>
<style lang="">
    
</style>