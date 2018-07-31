<template>
  <div class="row">
    <gallery :images="imgsSrc" :index="index" @close="index = null"></gallery>
    <imgdetail v-for="(image, imageIndex) in images"
               :key="imageIndex"
               :imgDetail="image"
               @click.native="index = imageIndex"></imgdetail>
  </div>
</template>

<script>
import VueGallery from 'vue-gallery';
import ImgDetail from './ImgDetail';
import img1 from '../assets/1.jpg';
import img2 from '../assets/2.jpg';
import img3 from '../assets/3.jpg';
import img4 from '../assets/4.jpg';

export default {
  name: 'MainPage',
  data() {
    return {
      images: [
        {
          src: img1,
          alt: 'Click to view',
          title: 'Title 1',
          category: 'Print, Branding',
        },
        {
          src: img2,
          alt: 'Click to view',
          title: 'Title 2',
          category: 'Print, Branding',
        },
        {
          src: img3,
          alt: 'Click to view',
          title: 'Title 3',
          category: 'Print, Branding',
        },
        {
          src: img4,
          alt: 'Click to view',
          title: 'Title 4',
          category: 'Print, Branding',
        },
      ],
      index: null,
    };
  },
  components: {
    gallery: VueGallery,
    imgdetail: ImgDetail,
  },
  computed: {
    // eslint-disable-next-line
    imgsSrc: function () {
      return this.images.map(img => img.src);
    },
  },
  methods: {
    // e
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
