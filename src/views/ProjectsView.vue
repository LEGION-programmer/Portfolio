<template>
    <div>
        <HeaderMain />
        <ProjectsPhotos />
        <ProjectsContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import ProjectsPhotos from '@/components/projectsPage/ProjectsPhotos.vue'
import ProjectsContent from '@/components/projectsPage/ProjectsContent.vue'

export default {
    name: 'ProjectsView',
    components: {
        HeaderMain,
        ProjectsPhotos,
        ProjectsContent
    }
}
</script>