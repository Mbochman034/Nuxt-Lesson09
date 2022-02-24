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
  }
}
</script>
