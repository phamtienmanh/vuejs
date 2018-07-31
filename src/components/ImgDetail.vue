<template>
  <div :class="className" class="text-center single-portfolio">
    <div class="">
      <img :src="imgDetail.src" :alt="imgDetail.alt || ''">
    </div>
    <div class="project-title light-bg">
      <a><h4 class="no-margin">{{imgDetail.title}}</h4></a>
      <p class="no-margin">{{imgDetail.category}}</p>
      <hr class="line">
    </div>
  </div>
</template>

<script>
export default {
  name: 'ImgDetail',
  data() {
    return {
      // e
    };
  },
  props: {
    className: {
      type: String,
      default: 'col-md-4',
    },
    imgDetail: {
      type: Object,
      default() {
        return {
          src: './assets/logo.png',
          alt: 'Click to view',
          title: '',
          category: '',
        };
      },
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  img {
    width: 100%;
    height: 100%;
  }
  h1, h2, h3, h4, h5, h6 {
    font-weight: 300;
    color: #646464;
    text-transform: capitalize;
  }
  p {
    font-size: 16px;
    color: #8e8e8e;
  }
  hr {
    margin: 6px auto auto;
    width: 42px;
  }
  .single-portfolio:hover {
    hr {
      background: #484848;
    }
  }
  .project-title {
    border: 1px solid #e5e5e5;
    border-top: 0;
    padding-top: 15px;
    padding-bottom: 15px;
    margin-bottom: 20px;
    & h4:hover{
      cursor: pointer;
    }
  }
</style>
