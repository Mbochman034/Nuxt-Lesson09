// I am using this as the default layout for all pages in the project. This would be useful for bigger projects I think.
<template>
    <div>
      <AppHeader/>
      <nuxt/>  
      <Footer/>
    </div>
</template>

<script>
import AppHeader from '../components/AppHeader';
import Footer from '../components/Footer';

export default {
  components: {
      AppHeader,
      Footer
  }
}
</script>
