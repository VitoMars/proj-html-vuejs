<template>
  <div class="header">
    <div class="nav-bar">
      <a href="#">
        <img src="../assets/img/avada-freelance-logo.png" alt="" />
      </a>
      <div class="buttons">
        <a href="#">
          <i class="fas fa-plus"></i>
        </a>
        <a href="#">
          <i class="fas fa-bars"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "~@fortawesome/fontawesome-free/css/all.min.css";
@import "./style/colors.scss";
.header {
  height: 100vh;
  width: 100vw;
  background-image: url("../assets/img/banner_images.png");
  background-size: cover;
  background-position: center;
}
.nav-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 15vh;
  width: 100vw;
  padding: 20px 50px;
  // background-color: $mirage;
}

i {
  font-size: 30px;
  padding: 15px;
  color: white;
}
</style>
