<template>
  <div class="header">
    <!-- Nav-bar -->
    <div class="nav-bar">
      <a href="">
        <img src="../assets/img/avada-freelance-logo.png" alt="" />
      </a>
      <div class="buttons">
        <i class="fas fa-plus"></i>
        <i class="fas fa-bars"></i>
      </div>
    </div>
    <!-- ArtDirector -->
    <div class="artDirector">
      <h2>AVADA FREELANCE</h2>
      <h1>Art Director</h1>
      <h3>IF IT DOESN’T CHALLENGE YOU, IT DOESN’T CHANGE YOU</h3>
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
  background-attachment: fixed;
}
.nav-bar {
  position: fixed;
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
  padding: 20px;
  color: white;
  cursor: pointer;
}

.artDirector {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}
h1 {
  font-size: 140px;
  letter-spacing: 1px;
  padding: 10px 0px;
  color: $radicalRed;
}
h2 {
  font-size: 20px;
  letter-spacing: 7px;
}
h3 {
  font-size: 14px;
  letter-spacing: 5px;
  font-weight: initial;
  color: $primary;
}
</style>
