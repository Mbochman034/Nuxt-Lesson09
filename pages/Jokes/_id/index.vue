<template>
  <div class="joke-page-wrapper">
    <nuxt-link class="btn btn-primary btn-md" to="/jokes">Back To Jokes</nuxt-link>
    <h2>{{ joke }}</h2>
    <hr>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      joke: {}
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data.joke;
    } catch (err) {
      console.log(err);
    }
  },
  head() {
    return {
      title: this.joke,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Best place for corny dad jokes"
        }
      ]
    };
  }
};
</script>

<style>
.joke-page-wrapper {
    padding: 2rem;
}
.joke-page-wrapper h2  {
    padding-top: 1.5rem;
}
</style>