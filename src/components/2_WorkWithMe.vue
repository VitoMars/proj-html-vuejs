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
    <!-- Circle -->
    <div class="box">
      <svg>
        <circle cx="100" cy="100" r="100"></circle>
      </svg>
      <div class="icon"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WorkWithMe",
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";

// Test 1
.box {
  position: relative;
  width: 300px;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  svg {
    position: relative;
    width: 220px;
    height: 220px;
    transform: rotate(-90deg);
    circle {
      width: 220px;
      height: 220px;
      fill: none;
      stroke-width: 10;
      stroke: $radicalRed;
      transform: translate(5px, 5px);
      stroke-dasharray: calc(100 * 6);
      stroke-dashoffset: calc((100 * 6) - ((100 * 6) * 95) / 100);
      stroke-linecap: round;
    }
  }
}

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
