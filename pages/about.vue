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
  },
  head: {
      title: 'About | The Potted Garden',
      meta: [
        {
          hid: 'About Us, how we got started with potted gardening',
          name: 'How we got started with potted gardenin',
          content: 'How we got started with potted gardenin'
        }
      ],
    }
};
</script>



