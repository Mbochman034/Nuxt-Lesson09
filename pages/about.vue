<template>
  <div>
    <Intro3/>
    <Popper/>
    <Search/>
  </div>
</template>

<script>
import Intro3 from '../components/Intro3.vue';
import Popper from '../components/Popper.vue';
import Search from '../components/Search.vue';

export default {
  name: 'Get Inspired',
  props: {
    msg: String
  },
  components: {
    Intro3,
    Popper,
    Search,
  }
}
</script>



