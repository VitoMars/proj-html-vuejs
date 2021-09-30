<template
  ><div>
    <AboutMe />
    <WorkWithMe />
  </div>
</template>

<script>
import AboutMe from "../components/1_AboutMe.vue";
import WorkWithMe from "../components/2_WorkWithMe.vue";
export default {
  name: "Main",
  components: {
    AboutMe,
    WorkWithMe,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat&family=Source+Sans+Pro&display=swap");
body {
  font-family: "Montserrat", Arial, Helvetica, sans-serif;
  h2 {
    font-size: 48px;
    letter-spacing: 1px;
  }
  h6 {
    font-size: 14px;
    letter-spacing: 4px;
    font-weight: inherit;
    margin: 20px 0px;
  }
  p {
    font-family: "Source Sans Pro", sans-serif;
    font-size: 18px;
    line-height: 30px;
    margin: 20px;
  }
  .separator {
    height: 1px;
    width: 5vw;
    margin-top: 10px;
    background-color: white;
  }
}
</style>
