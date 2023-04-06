<template>
    <div>
        <HeaderMain />
        <ExperiencePhoto />
        <ExperienceContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import ExperiencePhoto from '@/components/experiencePage/ExperiencePhoto.vue'
import ExperienceContent from '@/components/experiencePage/ExperienceContent.vue'

export default {
    name: 'ExperiemceView',
    components: {
        HeaderMain,
        ExperiencePhoto, 
        ExperienceContent
    }
}
</script>
