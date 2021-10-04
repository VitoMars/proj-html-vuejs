<template>
  <div class="trustedBy">
    <div class="container">
      <div class="flex-start">
        <!-- Img -->
        <img id="quotes" src="../assets/img/quotes-1.png" alt="" />
        <!-- Citazione -->
        <q>{{ this.quotes[this.counterText].quote }}</q>
        <!-- Autore -->
        <div id="author">{{ this.quotes[this.counterText].author }}</div>
        <!-- Cerchi -->
        <div class="circles">
          <i
            v-for="(quote, index) in quotes"
            :key="index"
            :class="index == counterText ? 'fas' : 'far'"
            class="fa-circle"
            @click="setQuote(index)"
          ></i>
        </div>
      </div>
      <!-- Trusted By -->
      <div class="flex-end">
        <h5>TRUSTED BY GLOBAL BRANDS</h5>
        <div class="brands">
          <img
            class="brand"
            v-for="n in 5"
            :key="n"
            :src="require('../assets/img/global_brand_' + n + '.png')"
            alt=""
          />
        </div>
      </div>
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
        {
          author: "Steve Jobs - Apple",
          quote:
            "That’s been one of my mantras — focus and simplicity. Simple can be harder than complex; you have to work hard to get your thinking clean to make it simple.",
        },
        {
          author: "Steve Jobs - Apple",
          quote:
            "I think if you do something and it turns out pretty good, then you should go do something else wonderful, not dwell on it for too long. Just figure out what’s next.",
        },
        {
          author: "Bill Gates - Microsoft",
          quote:
            "We all need people who will give us feedback. That's how we improve.",
        },
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
    setQuote(index) {
      this.counterText = index;
    },
    startRotation() {
      this.timer = setInterval(this.nextQuote, 5000);
    },
  },
  mounted() {
    this.startRotation();
  },
};
</script>

<style scoped lang="scss">
.trustedBy {
  display: flex;
  justify-content: center;
  height: 100vh;
  width: 100vw;
  background-image: url("../assets/img/testimonial_bkgd.jpg");
  background-position: center;
}

.container {
  height: 100vh;
  width: 70%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  padding: 50px 0px;
}

#quotes {
  margin-bottom: 50px;
}

q {
  max-width: 65vw;
  text-align: center;
}

i {
  padding: 5px;
  cursor: pointer;
}

h5 {
  margin: 50px;
}

#author {
  font-family: "Source Sans Pro", sans-serif;
  font-size: 18px;
  text-transform: uppercase;
  font-weight: bold;
  letter-spacing: 2px;
  padding-bottom: 25px;
}

.flex-start {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}

.flex-end {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
}

.brands {
  width: 90%;
  display: flex;
  justify-content: space-around;
}
</style>
