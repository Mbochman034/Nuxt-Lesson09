<template>
  <div>
    <section class="terms">
      <div class="w-75 my-4">
        <div class="accordion" role="tablist">
          <!-- for every terms in the object, toggle between showing content and hiding it each time user clicks -->
          <b-card v-for="(terms, key) in this.terms" :key="key" no-body class="my-2">
            <b-card-header header-tag="header" class="pt-2 pb-0" role="tab">
              <b-button block v-b-toggle="'accordion-'+key" variant="light">
                <h6>{{ terms.title }}</h6>
              </b-button>
            </b-card-header>
            <b-collapse :id="'accordion-'+key.toString()" accordion="my-accordion" role="tabpanel">
              <b-card-body class="text-start">
                <b-card-text>{{ terms.p1 }}</b-card-text>
                <b-card-text>{{ terms.p2 }} <a href="#"><span class="text-primary"></span></a></b-card-text>
              </b-card-body>
            </b-collapse>
          </b-card>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {
      terms: [
        {
          title: 'Annuals, Perennials, and Biennials',
          p1: 'Before you can successfully grow any plant, it is essential to understand its life cycle.',
          p2: 'Annuals are plants that complete their lifecycle (seed to flower) in a single growing season and then die; therefore they have to be planted new each year. Perennials are plants that come back year after year, while biennials take two growing seasons to complete their life cycle. Biennials do not flower the first year, but flower the second year, set seed, and then die.'
        },
        {
          title: 'Bolting',
          p1: 'Bolting occurs when a gardener does not harvest their crop, and the plants move past the peak edibility stage and into a flowering and seed production phase.',
          p2: 'For example, lettuces and cabbages should be harvested when the head is large and still firm, but if you allow them to continue their growth cycle, the heads will open up and a tall flower stalk will grow.'
        },
        {
          title: 'Companion Planting',
          p1: 'If you aren not in the know about companion planting, now it is the time to learn. Companion planting means planting different crops near each other because they benefit one another. This can help bring in pollinators, maximize planting space, or increase crop productivity.',
          p2: 'For example, planting marigoldsa around a garden helps repel garden pests while attracting pollinators.'
        }
      ]
    }
  }
}
</script>

<style>
.accordion {
  padding-left: 3rem;
}
</style>