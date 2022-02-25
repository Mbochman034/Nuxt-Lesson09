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
  },
  head: {
      title: 'Get Inspired | The Potted Garden',
      meta: [
        {
          hid: 'Get inspired by some of our most recent potted gardening projects',
          name: 'Get Inspired by potted gardening',
          content: 'Get Inspired by potted gardening'
        }
      ],
    }
};
</script>
