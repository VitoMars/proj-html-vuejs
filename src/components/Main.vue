<template>
  <div class="main">
    <AboutMe />
    <WorkWithMe />
    <RecentWork />
    <TrustedBy />
    <ExpertDesign />
    <ContactMe />
  </div>
</template>

<script>
import AboutMe from "../components/1_AboutMe.vue";
import WorkWithMe from "../components/2_WorkWithMe.vue";
import RecentWork from "../components/3_RecentWork.vue";
import TrustedBy from "../components/4_TrustedBy.vue";
import ExpertDesign from "../components/5_ExpertDesign.vue";
import ContactMe from "../components/6_ContactMe.vue";

export default {
  name: "Main",
  components: {
    AboutMe,
    WorkWithMe,
    RecentWork,
    TrustedBy,
    ExpertDesign,
    ContactMe,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat&family=Source+Sans+Pro&display=swap");
@import "./style/colors.scss";
body {
  font-family: "Montserrat", Arial, Helvetica, sans-serif;
  h2 {
    font-size: 48px;
    letter-spacing: 1px;
  }

  h5 {
    font-size: 17px;
    letter-spacing: 4px;
    line-height: 30px;
    font-weight: inherit;
    margin: 20px;
  }

  h6 {
    font-size: 14px;
    letter-spacing: 4px;
    line-height: 30px;
    font-weight: inherit;
    margin: 20px 0px;
  }

  p {
    font-family: "Source Sans Pro", sans-serif;
    font-size: 18px;
    line-height: 30px;
    margin: 20px;
  }

  q {
    font-family: "Source Sans Pro", sans-serif;
    font-size: 18px;
    font-style: italic;
    letter-spacing: 2px;
    line-height: 30px;
    padding: 25px;
  }

  input {
    font-family: "Source Sans Pro", sans-serif;
    padding: 0px 10px;
    height: 60px;
    width: 30vw;
    color: $input;
    border: none;
    outline: none;
  }

  .container-text {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .separator {
    height: 1px;
    width: 150px;
    margin-top: 10px;
    background-color: white;
  }
}
</style>
