<template>
  <div>
    <Intro2/>
    <Accordion/>
  </div>
</template>

<script>
import Intro2 from '../components/Intro2.vue';
import Accordion from '../components/Accordion.vue';

export default {
  name: 'Common Terms',
  props: {
    msg: String
  },
  components: {
    Intro2,
    Accordion,
  },
  head: {
        title: 'Common Terms | The Potted Garden',
        meta: [
          {
            hid: 'Browse common gardening terms',
            name: 'Browse common gardening terms',
            content: 'Browse common gardening terms'
          }
        ],
      }
};
</script>
