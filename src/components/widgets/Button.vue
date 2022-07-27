<template>
    <a v-if="btnType == 'primary'" :href="btnLink ? btnLink : '#'" class="btn btn-primary">Get started</a>
    <a v-if="btnType == 'secondary'" href="#" class="btn btn-secondary">Learn more</a>
</template>

<script>
export default {
  name: "HeroSection",
  props: {
    btnType: String,
    btnLink: String,
  }
};
</script>

<style lang="scss" scoped>
// Global Button Styles
.btn {
  font-weight: 700;
  padding: 1.1rem;
  border-radius: 1rem;
  position: relative;
  top: 0px;
  transition: top 0.3s ease;
  display: block;
  width: 225px;
  text-align: center;
  z-index: 1;
}

.btn-primary {
  background-color: var(--primary);
  color: #fff;

  &:after {
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
    top: -8px;

    &:after {
      top: 18px;
    }
  }
}

.btn-secondary {
  background-color: var(--primary-light);
  color: var(--primary);


  &:hover {
    top: -8px;
  }
}
</style>
