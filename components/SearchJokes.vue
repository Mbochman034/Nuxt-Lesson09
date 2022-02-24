<template>
  <div class="joke-container">
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="text" placeholder="Type a word...">
    <input class="btn btn-primary btn-md"  type="submit" value="Search Jokes">
  </form>
  </div>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: ""
    };
  },
  methods: {
    onSubmit() {
      this.$emit("search-text", this.text);
      this.text = "";
    }
  }
};
</script>

<style>
.joke-container {
    padding: 2rem;
}
input {
    width: 10em;
}
</style>