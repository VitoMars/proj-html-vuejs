<template>
  <div class="recentWork">
    <h2>Recent Work</h2>
    <h6>WEB • BRANDING • UX/UI</h6>
    <div class="separator"></div>

    <div class="imgs">
      <div v-for="n in 6" :key="n" class="picture">
        <img
          :mouseover="getText(n)"
          :src="require('../assets/img/portfolio' + n + '_featured_item.jpg')"
          alt=""
        />
        <span>{{ text }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecentWork",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    getText(n) {
      if (n == 1) return (this.text = "flat picture frames");
      else if (n == 2) return (this.text = "a bag for life");
      else if (n == 3) return (this.text = "beyond labels");
      else if (n == 4) return (this.text = "and the ampersand");
      else if (n == 5) return (this.text = "running man");
      else if (n == 6) return (this.text = "the notebook");
    },
  },
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";
.recentWork {
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 200px 0px;
  background-color: $olivine;
}

.imgs {
  display: flex;
  flex-wrap: wrap;
  margin-top: 100px;
  background-color: $radicalRedVibrant;
}

.picture {
  position: relative;
}

img {
  width: 50vw;
  vertical-align: top;
}

span {
  display: none;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  //   display: flex;
  justify-content: center;
  align-items: center;
  font-size: 30px;
  text-transform: uppercase;
}

img:hover {
  opacity: 0.1;
}

img:hover span {
  display: flex !important;
}
</style>
