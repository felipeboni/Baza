<template onscroll="onScroll">
  <!-- Every section is divided by components  -->
  <Navbar/>
  <Hero class="hero"/>
  <Tiles class="section"/>
  <CallToAction class="section"/>
  <Stats class="section"/>
  <Steps class="section"/>
  <Feedbacks class="section"/>
  <PricingTable class="section"/>
</template>

<script>
import Navbar from './components/layout/Navbar.vue'
import Hero from './components/Hero.vue'
import Tiles from './components/Tiles.vue'
import CallToAction from './components/CallToAction.vue'
import Stats from './components/Stats.vue'
import Steps from './components/Steps.vue'
import Feedbacks from './components/Feedbacks.vue'
import PricingTable from './components/PricingTable.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Hero,
    Tiles,
    CallToAction,
    Stats,
    Steps,
    Feedbacks,
    PricingTable
  },
  created () {
    window.addEventListener('scroll', this.onScroll);
  },
  mounted() {
    // if (document.readyState == "complete") {
      document.getElementsByClassName('hero')[0].classList.add("loaded");
    // }
  },
  unmounted () {
    window.removeEventListener('scroll', this.onScroll);
  },
  data () {
    return {
      offsetTop: window.pageYOffset || document.documentElement.scrollTop
    }
  },
  watch: {
    offsetTop () {
       this.callbackFunc()
    }
  },
  methods: {
    onScroll () {
      this.offsetTop = window.pageYOffset || document.documentElement.scrollTop
    },
    isElementInViewport(el) {
      var rect = el.getBoundingClientRect();
      return (
        rect.top >= 0 &&
        rect.left >= 0 &&
        rect.bottom - 250 <= (window.innerHeight || document.documentElement.clientHeight) &&
        rect.right <= (window.innerWidth || document.documentElement.clientWidth)
      );
    },
    callbackFunc() {
      let items = document.querySelectorAll(".section");
      for (var i = 0; i < items.length; i++) {
        if (this.isElementInViewport(items[i])) {
          items[i].classList.add("in-view");
        }
      }
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;800;900&display=swap');

// Global variables
:root {
  --background: #ffffff;
  --dark: #16252e;
  --primary: #155ce7;
  --primary-light: #e0e7fa;
  --secondary: #54595F;
  --text-body: #7A7A7A;
  --text-accent: #61CE70;
  --font-family: 'Roboto', sans-serif;
}

// START::Remove default styling
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  overflow-x: hidden;
}

body {
  font-family: var(--font-family);
  color: var(--dark);
  background: var(--background);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

a {
  text-decoration: none;
  color: inherit;
}

ul {
  list-style: none;
}

button, input[type="submit"], input[type="reset"] {
	background: none;
	color: inherit;
	border: none;
	padding: 0;
	font: inherit;
	cursor: pointer;
	outline: inherit;
}
// END::Remove default styling

// Global Container Styles
.container {
  max-width: 1160px;
  padding: 0 20px;
  margin: 0 auto;
}

// Load animations
/* .section {
  visibility: hidden;
  opacity: 0;
  transform: translateY(7%);
  transition: all 0.3s ease;
}
.in-view {
  visibility: visible;
  opacity: 1;
  transform: translateY(0%);
}
.loaded {
  animation: fadeIn 0.3s ease;
} */

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(7%);
  }
  to {
    opacity: 1;
    transform: translateY(0%);
  }
}
</style>
