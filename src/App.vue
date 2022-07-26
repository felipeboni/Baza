<template>
  <Navbar/>
  <Hero/>
  <Tiles/>
</template>

<script>
import Navbar from './components/layout/Navbar.vue'
import Hero from './components/Hero.vue'
import Tiles from './components/Tiles.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Hero,
    Tiles
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

// Global Button Styles
.btn-primary {
  font-weight: 700;
  padding: 1.1rem 4rem;
  border-radius: 1rem;
  background-color: var(--primary);
  color: #fff;
  position: relative;
  top: 0px;
  transition: top 0.3s;

  &:before {
    content: '';
    position: absolute;
    top: 10px;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 1rem;
    z-index: -1;
    filter: blur(25px);
    background-color: rgba(21, 92, 231, 0.5);
    transition: top 0.3s;
  }

  &:hover {
    top: -5px;

    &:before {
      top: 15px;
    }
  }
}

.btn-secondary {
  font-weight: 700;
  padding: 1.1rem 4rem;
  border-radius: 1rem;
  background-color: var(--primary-light);
  color: var(--primary);
  position: relative;
  top: 0px;
  transition: top 0.3s;

  &:hover {
    top: -5px;
  }
}
</style>
