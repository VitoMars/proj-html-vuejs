<template>
  <div class="workWithMe">
    <h2>Why Work With Me</h2>
    <h6>WEB • BRANDING • UX/UI</h6>
    <div class="separator"></div>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
      commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla.
    </p>
  </div>
</template>

<script>
export default {
  name: "WorkWithMe",
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";
.workWithMe {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding-top: 200px;
  height: 100vh;
  background-color: $secondary;
}

h6 {
  color: $text-secondary;
}

p {
  max-width: 900px;
  color: $text-primary;
}
</style>
