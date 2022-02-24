<template>
<div class="search-container">
<div class="row pb-5">
  <h3 class="col-8 pt-1 pb-1">Do you need another plant?</h3>
  <p class="lead col-sm-12 pb-5">Use the search field below to see if you need another plant.</p>
  <!-- Search Bar -->
  <section class="col-sm-12">
    <div class="input-group">
      <input type="text" class="form-control" placeholder="Enter your plant name here. " aria-label="Search item" aria-describedby="basic-addon2">
      <div class="input-group-append">
        <button class="btn btn-primary btn-md" type v-on:click="show = !show" v-bind:key="msg">Do I need this plant?</button>
      </div>
    </div>
    <!-- if-else statement -->
    <p class="ml-2 pt-3" v-if="show"><i>Type any plant name, any at all.</i></p>
    <p class="ml-2 pt-3" v-else><i>Absolutely, get one immediately!</i></p>
  </section>
</div>
</div>
</template>


<script>
export default {
  data () {
      return {
        show: true
      }
  }
}
</script>

<style>
.search-container {
  padding: 0 3rem 1rem 3rem;
}
</style>