<template>
    <div>
        <HeaderMain />
        <MediaPhotos />
        <MediaContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue';
import MediaPhotos from '../components/mediaPage/MediaPhotos.vue'
import MediaContent from '../components/mediaPage/MediaContent.vue'

export default {
    name: 'MediaView',
    components: {
        HeaderMain,
        MediaPhotos,
        MediaContent
    }
}
</script>
<style lang="">
    
</style>