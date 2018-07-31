<template>
  <div id="app" class="light-bg">
    <div class="container">
      <div class="header"></div>
      <div class="content">
        <router-view/>
      </div>
      <div class="footer"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      // e
    };
  },
};
</script>

<style lang="scss">
  @import './styles/custom-bootstrap.scss';
  @import '../node_modules/bootstrap/scss/bootstrap.scss';

  html, body, #app {
    height: 100%;
  }
  #app {
    overflow: auto;
  }
  .light-bg {
    background: #f6f6f6 none repeat scroll 0 0;
  }
  .header {
    height: 20px;
  }
  .blueimp-gallery > a {
    color: #fff !important;
  }
  .no-margin {
    margin: 0;
  }
</style>
