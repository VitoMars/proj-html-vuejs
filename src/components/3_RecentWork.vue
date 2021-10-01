<template>
  <div class="recentWork">
    <h2>Recent Work</h2>
    <h6>WEB • BRANDING • UX/UI</h6>
    <div class="separator"></div>

    <div class="imgs">
      <img
        v-for="n in 6"
        :key="n"
        :src="require('../assets/img/portfolio' + n + '_featured_item.jpg')"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "RecentWork",
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";
.recentWork {
  //  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 200px 0px;
  background-color: $olivine;
}

.imgs {
  padding-top: 50px;
}

.imgs img {
  width: 50vw;
  vertical-align: top;
}
</style>
