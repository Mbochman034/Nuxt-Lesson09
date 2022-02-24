<template>
  <!-- Container -->
  <b-container class="images">
    <b-row>
      <!-- ImgCard component pulled from its own file and using props for all attributes -->
      <ImgCard
        v-for="(imgList, index) in images"
        :key="index"
        :imgList="imgList"
        :src="imgList.imageSR"
        :alt="imgList.alt"
        :title="imgList.title"
        :text="imgList.text"
        :btn_text="imgList.btn_text"
      />
    </b-row>
  </b-container>
  <!-- Container End -->
</template>

<!-- All content is from variables in the <script> section of the .vue file. -->
<script>
// ImgCard component imported from its own component
import ImgCard from "../components/ImgCard";

export default {
  name: "Images",
  // add ImgCard component so it can be used in the template
  components: { ImgCard },
  data() {
    return {
      header: "Images / Cards",
      subtitle:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit, Eos repudiandae officiis dolores perspiciatis pariatur culpa.",
      images: [
        {
          title: "Outdoor Spaces",
          text:
            "Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui...",
          btn_text: "Toggle Image Border",
          url:
            "https://i.ibb.co/9HsVZZt/best-planters-and-containers-1618332662.jpg",
          alt: "Picture of outdoor patio with plants",
        },
        {
          title: "Starting Seedlings",
          text:
            "Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui...",
          btn_text: "Toggle Image Border",
          url:
            "https://i.ibb.co/16Rg5Gh/seedlings-1.jpg",
          alt: "Green seedling plants sprouting from soil",
        },
        {
          title: "Indoor Spaces",
          text:
            "Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui...",
          btn_text: "Toggle Image Border",
          url:
            "https://i.ibb.co/M9ZJFZZ/sunroom.jpg",
          alt: "Image of modern sunroom with potted plants",
        },
      ],
    };
  },
};
</script>

<style>
.images {
  margin-top: 3.75rem;
  margin-left: 4rem;
}
.images-container {
  padding-left: 2rem;
}
</style>