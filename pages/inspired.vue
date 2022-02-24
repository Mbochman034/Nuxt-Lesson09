<template>
  <div>
    <Intro1/>
    <Gallery/>
  </div>
</template>

<script>
import Intro1 from '../components/Intro1.vue';
import Gallery from '../components/Gallery.vue';

export default {
  name: 'Get Inspired',
  props: {
    msg: String
  },
  components: {
    Intro1,
    Gallery,
  }
}
</script>
