
<template>
  <div>
    <Jumbotron/>
    <HomeCards/>
  </div>
</template>

<script>
import Jumbotron from '../components/Jumbotron.vue';
import HomeCards from '../components/HomeCards.vue';

export default {
  name: 'IndexPage',
  props: {
    msg: String
  },
  components: {
    Jumbotron,
    HomeCards,
  },
  head: {
      title: 'Home |  The Potted Garden',
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