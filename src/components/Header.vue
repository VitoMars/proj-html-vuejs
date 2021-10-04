<template>
  <div class="header">
    <!-- Nav-bar -->
    <div class="nav-bar" :class="this.ticking ? 'scrollTrue' : ''">
      <a href="">
        <img src="../assets/img/avada-freelance-logo.png" alt="" />
      </a>
      <div class="buttons">
        <i class="fas fa-plus"></i>
        <i class="fas fa-bars"></i>
      </div>
    </div>
    <div class="icons">
      <div class="icon">
        <i class="fas fa-folder-open"></i>
        <span>Demos</span>
      </div>
      <div class="icon">
        <i class="fas fa-cart-plus"></i>
        <span>Buy Now</span>
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
  data() {
    return {
      lastKnownScrollPosition: 0,
      ticking: false,
    };
  },
  methods: {
    scroll() {
      document.addEventListener("main", function() {
        this.lastKnownScrollPosition = window.scrollY;

        if (!this.ticking) {
          window.requestAnimationFrame(function() {
            this.ticking = false;
          });
          this.ticking = true;
        }
      });
    },
  },
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
  z-index: 1;
  // background-color: $primary;
}

.scrollTrue {
  background-color: $primary;
}

.icons {
  position: fixed;
  top: 15%;
  left: 95%;
  z-index: 1;
}

.icon {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 66px;
  width: 66px;
  border-radius: 10px;
  margin: 10px;
  background-color: white;
  cursor: pointer;
}

.icon i,
.icon span {
  color: $snipGrayDarkMuted;
  color: #4a5259;
  color: #33475b;
  color: $mirage;
  // color: $shark;
}

.icon i {
  font-size: 25px;
}

.icon span {
  font-size: 12px;
  font-weight: bold;
  padding-top: 7px;
}

.buttons i {
  font-size: 30px;
  padding: 20px;
  cursor: pointer;
  transition: 0.3s linear;
}

.buttons i:hover {
  color: $radicalRed;
}

.fa-bars {
  color: $radicalRed;
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
  color: $text-primary;
}
</style>
