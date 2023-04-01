<template>
  <div>

    <HeaderMain/>
    <MyPhotos/>
    <ContentMain/>

  </div>
</template>

<script>
import HeaderMain from '../components/HeaderMain.vue'
import MyPhotos from '../components/MyPhotos.vue'
import ContentMain from '../components/ContentMain.vue'

export default {
  name: 'HomeView',
  components: {
    HeaderMain,
    MyPhotos,
    ContentMain
  }
}
</script>
