<template>
  <div
    class="arianna"
    @click="shuffle"
  >
    <transition
      name="fade"
      :duration="{ enter: 500, leave: 0 }"
    >
      <div
        class="content"
        :key="currentQuote"
      >
        <div>
          <img
            class="picture"
            src="../assets/ariannella.png"
          />
        </div>
        <pre>{{currentQuote}}</pre>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'Arianna',
  props: {
    quotes: Array
  },
  data: () => {
    return {
      currentIndex: 0,
      shuffling: true
    }
  },
  mounted () {
    this.shuffle()
  },
  methods: {
    shuffle () {
      this.currentIndex = this.getRandomInt(0, this.quotes.length - 1)
    },
    getRandomInt (min, max) {
      min = Math.ceil(min);
      max = Math.floor(max);
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }
  },
  computed: {
    currentQuote () {
      return this.quotes && this.quotes[this.currentIndex] || ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.arianna {
  font-size: 2.5rem;
  display: flex;
  flex-direction: column;
  flex: 11;
  justify-content: center;
  justify-items: center;
  font-weight: bold;
  cursor: pointer;
}

.content {
  display: flex;
  justify-content: center;
  justify-items: center;
  flex-direction: column;
}

.picture {
  border-radius: 50%;
  width: 10rem;
  height: 10rem;
}

.fade-enter-active {
  transition: opacity 0.5s;
}
.fade-enter {
  opacity: 0;
}
</style>
