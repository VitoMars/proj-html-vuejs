<template>
  <div class="trustedBy">
    <div class="container">
      <img id="quotes" src="../assets/img/quotes-1.png" alt="" />
      <q>
        {{ this.quotes[this.counterText] }}
      </q>
    </div>
  </div>
</template>

<script>
export default {
  name: "TrustedBy",
  data() {
    return {
      counterText: 0,
      quotes: [
        "That’s been one of my mantras — focus and simplicity. Simple can be harder than complex; you have to work hard to get your thinking clean to make it simple.",
        "I think if you do something and it turns out pretty good, then you should go do something else wonderful, not dwell on it for too long. Just figure out what’s next.",
      ],
      timer: null,
    };
  },
  methods: {
    nextQuote() {
      this.counterText += 1;
      if (this.counterText > this.quotes.length - 1) {
        this.counterText = 0;
      }
    },
    startRotation() {
      this.timer = setInterval(this.nextQuote, 2000);
    },
  },
  mounted() {
    this.startRotation();
  },
};
</script>

<style scoped lang="scss">
.trustedBy {
  height: 100vh;
  width: 100vw;
  background-image: url("../assets/img/testimonial_bkgd.jpg");
  background-position: center;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}
#quotes {
  margin-top: 150px;
  margin-bottom: 50px;
}

q {
  max-width: 60%;
  font-style: italic;
  font-size: 18px;
  letter-spacing: 2px;
  line-height: 30px;
  text-align: center;
  padding: 25px;
}
</style>
