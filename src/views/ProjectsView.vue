<template>
    <div>
        <HeaderMain />
        <PhotoSlider :items="photos"/>
        <ProjectsContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import PhotoSlider from '@/components/PhotoSlider.vue'
import ProjectsContent from '@/components/projectsPage/ProjectsContent.vue'
import photo1 from '../assets/projects/photo1.jpg'
import photo2 from '../assets/projects/photo2.jpg'
import photo3 from '../assets/projects/photo3.jpg'
import photo4 from '../assets/projects/photo4.jpg'
import photo5 from '../assets/projects/photo5.jpg'

export default {
    name: 'ProjectsView',
    components: {
        HeaderMain,
        PhotoSlider,
        ProjectsContent
    },
    setup(){
      const photos = [
        photo1, photo2, photo3, photo4, photo5
      ]

      return {photos}
    }
}
</script>