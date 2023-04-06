<template>
    <div>
        <HeaderMain />
        <ContactPhotos />
        <ContactContent />
    </div>
</template>
<script>
import HeaderMain from '@/components/HeaderMain.vue'
import ContactPhotos from '@/components/contactPage/ContactPhotos.vue'
import ContactContent from '@/components/contactPage/ContactContent.vue'

export default {
    name: 'ContactView',
    components: {
        HeaderMain,
        ContactPhotos,
        ContactContent
    }
}
</script>
