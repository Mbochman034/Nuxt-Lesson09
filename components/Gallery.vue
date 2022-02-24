<template>
 <!-- Fills out and binds attributes from the object array to RecipeItemCard components -->
            <main class="main__primary-container col-sm-12">
              <section class="main__menu-list"> 
                <RecipeItemCard 
                v-for="item in items" 
                v-bind:key="item.key"
                v-bind:recipeName="item.recipeName"
                v-bind:text="item.text"
                v-bind:imageSrc="item.imageSrc"
                />
              </section>
          </main>
</template>

<script>
import RecipeItemCard from '@/components/RecipeItemCard.vue'

export default {
  name: 'RecipeItems',
  components: {
    RecipeItemCard
  },
  props: {},
  data() {
    return { items:
      [
        { id: 1, recipeName:"Lavendar", imageSrc:"image1.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." },
        { id: 2, recipeName:"Potato Vine", imageSrc:"image2.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." },
        { id: 3, recipeName:"Window Boxes", imageSrc:"image3.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." },
        { id: 4, recipeName:"Pet-Friendly Plants", imageSrc:"image4.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." },
        { id: 5, recipeName:"Small Spaces", imageSrc:"image5.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." },
        { id: 6, recipeName:"Herbs", imageSrc:"image6.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." },
        { id: 7, recipeName:"Get Your Hands Dirty", imageSrc:"image7.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." },
        { id: 8, recipeName:"Patio Color", imageSrc:"image8.jpg", text:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua." }

      ]
      }
  }
}
</script>

<style>
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
}
.main__menu-list {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-evenly;
}
.main__primary-container {
  padding: 3rem;
}
</style>