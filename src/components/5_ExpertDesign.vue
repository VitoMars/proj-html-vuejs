<template>
  <div class="ExpertDesign">
    <div class="razor-blade"></div>
    <div class="container-text">
      <h2>Expert Design Advice</h2>
      <h6>TRENDING DESIGN NEWS</h6>
      <div class="separator"></div>
    </div>
    <div class="container-img">
      <div class="picture" v-for="n in 3" :key="n">
        <div class="img">
          <img
            :mouseover="getText(n)"
            :src="require('../assets/img/blog' + n + '-featured.jpg')"
            alt=""
          />
          <span>{{ text }}</span>
        </div>
        <div class="box-text">
          <h3>{{ text }}</h3>
          <p>
            What's to come next? Lorem ipsum dolor sit amet, consectetur
            adipiscing elit, sed do eiusmod tempor incididunt ut labore et
            dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExpertDesign",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    getText(index) {
      if (index == 1) return (this.text = "Live The Design Process");
      else if (index == 2) return (this.text = "What's Next of the App Store?");
      else if (index == 3) return (this.text = "The Humble Wooden Desk");
    },
  },
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";
.ExpertDesign {
  width: 100vw;
  background-color: $kashmirBlue;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-items: center;
}

.container-img {
  display: flex;
  flex-wrap: wrap;
  margin-top: 100px;
  cursor: pointer;
  background-color: $secondary;
}

.box-text {
  width: calc(100vw / 3);
  margin-bottom: 50px;
}

.picture {
  position: relative;
}

.img {
  position: relative;
  background-color: $radicalRed;
}

img {
  width: calc(100vw / 3);
  vertical-align: top;
  background-color: $radicalRed;
  transition: all 0.5s linear;
}

span {
  display: none;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  align-items: center;
  font-size: 20px;
}

img:hover {
  opacity: 0.1;
}

.img:hover span {
  display: flex;
}

h3 {
  font-size: 28px;
  color: $radicalRed;
  letter-spacing: 1px;
  margin: 20px;
  margin-top: 30px;
  line-height: 40px;
}

p {
  color: $text-primary;
}

// Razor-Blade
.razor-blade {
  position: relative;
  padding-top: 100px;
  width: 100%;
  height: 100px;
  background: $kashmirBlue;
}

.razor-blade::before {
  position: absolute;
  width: 100%;
  height: 100%;
  content: "";
  background: inherit;
  inset: 0;
  transform-origin: bottom left;
  transform: skewY(-3deg);
}
</style>
