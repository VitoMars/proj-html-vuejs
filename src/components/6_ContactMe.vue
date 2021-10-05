<template>
  <div class="contactMe">
    <div class="container-main">
      <!-- Titoli -->
      <div class="container-text">
        <h2>Let’s Work Together</h2>
        <h6>TELL ME MORE ABOUT YOUR PROJECT</h6>
        <div class="separator"></div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco.
        </p>
      </div>
      <!-- Vari input -->
      <div class="container-input">
        <input type="text" placeholder="NAME*" />
        <input type="text" placeholder="EMAIL*" />
        <input type="text" placeholder="PHONE" />
        <button>Let's Talk</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactMe",
};
</script>

<style scoped lang="scss">
@import "./style/colors.scss";

.contactMe {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
  background-color: $gallery;
}

.container-main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  max-width: 50%;
}

.container-input {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h2 {
  color: #1d1d1d;
}

h6 {
  color: $text-primary;
}

p {
  color: $input;
  text-align: center;
}

input,
button {
  margin: 20px;
}

button {
  font-family: Montserrat;
  height: 60px;
  width: 30vw;
  font-size: 18px;
  letter-spacing: 4px;
  text-align: center;
  color: white;
  background-color: $radicalRed;
  border: none;
  text-transform: uppercase;
  cursor: pointer;
}

button:hover {
  color: $radicalRed;
  background-color: white;
}

.separator {
  background-color: #b9bfcc;
}
</style>
