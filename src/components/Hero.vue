<template>
  <section>
    <div class="container">
      <div class="hero-text">
        <img
          class="bg-img-left"
          src="../assets/11.png"
          alt="Man touching a lamp"
        />
        <h1>Think less about tracking numbers, more about your bussiness.</h1>
        <span
          >Our app help you to save time on tracking the activity, time,
          earnings, and more. Take everything under control with Baza.</span
        >
        <img
          class="bg-img-right"
          src="../assets/1.png"
          alt="Woman carrying files"
        />
      </div>
      <div class="hero-buttons">
        <!-- <button type="button" class="btn-primary">Get started</button> -->
        <Button btn-type="primary" />
        <Button btn-type="secondary" />
      </div>

      <div class="hero-img">
        <img
          src="../assets/3.png"
          alt="System dashboard view"
          draggable="false"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Button from './widgets/Button.vue'

export default {
  name: "HeroSection",
  components: {
    Button
  }
    
};
</script>

<style lang="scss" scoped>
.container {
  padding-top: 1rem;
  text-align: center;

  @media screen and (min-width: 768px) {
    padding-top: 6rem;
  }

  .hero-text {
    position: relative;
    max-width: 65ch;
    margin: 0 auto;

    h1 {
      font-size: 2.6rem;
      font-weight: 800;
    }

    @media screen and (min-width: 768px) {
      h1 {
        font-size: 3.3rem;
      }
    }

    span {
      display: block;
      margin-top: 1rem;
      font-size: 1.2rem;
      color: var(--text-body);
      padding: 0 0.5rem;
      line-height: 150%;
      letter-spacing: 0.5px;
    }

    .bg-img-right {
      position: relative;
      width: 80%;
      margin-top: 2rem;
    }

    .bg-img-left {
      position: absolute;
      width: 100%;
      max-width: 480px;
      left: -120%;
      top: 0px;
      z-index: -2;
    }

    @media screen and (min-width: 768px) {
      .bg-img-right {
        position: absolute;
        width: 100%;
        max-width: 500px;
        right: -100%;
        top: 0px;
        z-index: -2;
      }
    }
  }

  .hero-buttons {
    display: grid;
    grid-template-columns: repeat(auto-fill, 225px);
    max-width: 500px;
    margin: 3rem auto 0 auto;
    justify-content: center;
    gap: 1rem;
  }

  @media screen and (min-width: 768px) {
    .hero-buttons {
      gap: 3rem;
    }
  }

  .hero-img {
    margin: 4rem auto 0 auto;
    // animation: float 3s ease infinite alternate;

    img {
      border-radius: 2rem;
      box-shadow: 0px 20px 50px rgba(0, 0, 0, 0.2);
      max-width: 100%;
    }

    @media screen and (min-width: 768px) {
      margin: 9rem auto 0 auto;

      img {
        max-width: 80%;
      }
    }
    
  }
}

@keyframes float {
      from {
        transform: translateY(2%);
      }
      to {
        transform: translateY(-2%);
      }
    }
</style>
