<template>
  <div class="joke-wrapper">
    <Intro4/>
    <SearchJokes v-on:search-text="searchText"/>
    <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke"/>
  </div>
</template>

<script>
import Intro4 from '../../components/Intro4.vue';
import axios from "axios";
import Joke from "../../components/Joke";
import SearchJokes from "../../components/SearchJokes";
export default {
  components: {
    Intro4,
    Joke,
    SearchJokes
  },
  data() {
    return {
      jokes: []
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get("https://icanhazdadjoke.com/search", config);
      this.jokes = res.data.results;
    } catch (err) {
      console.log(err);
    }
  },
  methods: {
    async searchText(text) {
      const config = {
        headers: {
          Accept: "application/json"
        }
      };
      try {
        const res = await axios.get(
          `https://icanhazdadjoke.com/search?term=${text}`,
          config
        );
        this.jokes = res.data.results;
      } catch (err) {
        console.log(err);
      }
    }
  },
  head() {
    return {
      title: "Jokes | The Potted Garden",
      meta: [
        {
          hid: "Jokes for Days",
          name: "Jokes for Days",
          content: "Best place for corny dad jokes"
        }
      ]
    };
  }
};
</script>

<style>
.joke-wrapper {
  padding: 1rem 2rem 1rem 2rem;
}
</style>