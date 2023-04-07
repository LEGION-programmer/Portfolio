<template>
    <div>
        <HeaderMain />
        <PhotoSlider :items="photos"/>
        <ContactContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import PhotoSlider from '@/components/PhotoSlider.vue'
import ContactContent from '@/components/contactPage/ContactContent.vue'
import photo1 from '../assets/contact/photo1.jpg'
import photo2 from '../assets/contact/photo2.jpg'
import photo3 from '../assets/contact/photo3.jpg'
import photo4 from '../assets/contact/photo4.jpg'
import photo5 from '../assets/contact/photo5.jpg'

export default {
    name: 'ContactView',
    components: {
        HeaderMain,
        PhotoSlider,
        ContactContent
    },
    setup(){
      const photos = [
        photo1, photo2, photo3, photo4, photo5
      ]

      return {photos}
    }
}
</script>
