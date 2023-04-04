<template>
    <div>
        <HeaderMain />
        <AboutPhotos />
        <AboutContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue';
import AboutPhotos from '@/components/aboutPage/AboutPhotos.vue';
import AboutContent from '@/components/aboutPage/AboutContent.vue';

export default {
    name: 'AboutView',
    components: {
        HeaderMain,
        AboutPhotos,
        AboutContent
    }
}
</script>
