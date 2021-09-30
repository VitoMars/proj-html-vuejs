<template>
  <div class="footer">
    <img src="../assets/img/avada-footer-logo-66x66.png" alt="" />
    <span
      >© Copyright 2012 - 2021 | Avada Theme by
      <a href="https://theme-fusion.com">ThemeFusion</a> | All Rights Reserved |
      Powered by <a href="https://wordpress.org">WordPress</a>
    </span>
    <div class="socials">
      <a href="">
        <i class="fab fa-facebook-square"></i>
      </a>
      <a href="">
        <i class="fab fa-twitter-square"></i>
      </a>
      <a href="">
        <i class="fab fa-instagram-square"></i>
      </a>
      <a href="">
        <i class="fab fa-youtube-square"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";
.footer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 50vh;
  width: 100vw;
  background-color: $primary;
}

img {
  height: 100px;
  width: 100px;
}

span {
  margin-top: 50px;
  margin-bottom: 20px;
  color: $text-primary;
}
a {
  color: white;
  text-decoration: none;
}

i {
  font-size: 40px;
  margin: 5px;
  padding: 7px;
}
</style>
