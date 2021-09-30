<template>
  <div class="AboutMe">
    <div class="title">
      <h2>About Me</h2>
      <h6>UI & UX EXPERT</h6>
      <span class="separator"></span>
    </div>
    <div class="paragraphs">
      <div class="left">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </p>
        <p>
          Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
          dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est
          laborum. Sed ut perspiciatis unde omnis iste natus error sit
          voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque
          ipsa quae ab illo inventore veritatis et quasi architecto beatae.
        </p>
      </div>
      <div class="right">
        <p>
          Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
          dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est
          laborum. Sed ut perspiciatis unde omnis iste natus error sit
          voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque
          ipsa quae ab illo inventore.
        </p>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About Me",
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";
.AboutMe {
  height: 100vh;
  width: 100vw;
  padding: 90px 30px 0px 30px;
  background-color: $mirage;
}

.title {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.separator {
  height: 1px;
  width: 5vw;
  margin-top: 10px;
  background-color: white;
}

.paragraphs {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.left,
.right {
  margin: 0px 20px;
}

p {
  max-width: 550px;
  color: $primary;
}

h6 {
  color: $secondary;
}
</style>
