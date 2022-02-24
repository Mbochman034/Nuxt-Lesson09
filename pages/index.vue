
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
  }
}
</script>
