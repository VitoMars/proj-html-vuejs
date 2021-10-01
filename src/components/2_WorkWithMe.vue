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
    <!-- Circles -->
    <div class="circles">
      <!-- Box 1 -->
      <div class="box">
        <div class="relative">
          <svg>
            <circle cx="100" cy="100" r="100"></circle>
          </svg>
          <div class="icon">
            <i class="fas fa-drafting-compass"></i>
          </div>
          <h5>WEB DESIGN</h5>
        </div>
      </div>
      <!-- Box2 -->
      <div class="box">
        <div class="relative">
          <svg>
            <circle cx="100" cy="100" r="100"></circle>
          </svg>
          <div class="icon">
            <i class="fas fa-shield-alt"></i>
          </div>
          <h5>WEB BRANDING</h5>
        </div>
      </div>
      <!-- Box 3 -->
      <div class="box">
        <div class="relative">
          <svg>
            <circle cx="100" cy="100" r="100"></circle>
          </svg>
          <div class="icon">
            <i class="far fa-gem"></i>
          </div>
          <h5>UI / UX</h5>
        </div>
      </div>
    </div>
    <div class="razor-blade"></div>
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
  background-color: $secondary;
}

h6 {
  color: $text-secondary;
}

h5 {
  font-size: 14px;
  letter-spacing: 4px;
  font-weight: inherit;
  margin-top: 50px;
}

p {
  max-width: 900px;
  color: $text-primary;
}

// Cerchi
.circles {
  width: 70vw;
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
  .box {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .relative {
      position: relative;
      width: 210px;
      height: 210px;
      svg {
        position: relative;
        max-width: 210px;
        height: 210px;
        transform: rotate(-90deg);
        circle {
          width: 200px;
          height: 200px;
          fill: none;
          stroke-width: 10px;
          stroke: $radicalRed;
          transform: translate(5px, 5px);
          stroke-dasharray: calc(100 * 6);
          stroke-linecap: round;
        }
      }
    }
  }
}

.circles .box:nth-child(1) svg circle {
  stroke-dashoffset: calc((100 * 6) - ((100 * 6) * 92) / 100);
}

.circles .box:nth-child(2) svg circle {
  stroke-dashoffset: calc((100 * 6) - ((100 * 6) * 85) / 100);
}

.circles .box:nth-child(3) svg circle {
  stroke-dashoffset: calc((100 * 6) - ((100 * 6) * 99) / 100);
}

.icon {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 60px;
  color: $text-primary;
}

// Razor-Blade
.razor-blade {
  position: relative;
  width: 100%;
  height: 100px;
  background: $secondary;
}

.razor-blade::after {
  position: absolute;
  width: 100%;
  height: 100%;
  content: "";
  background: inherit;
  inset: 0;
  transform-origin: top right;
  transform: skewY(-4deg);
}
</style>
