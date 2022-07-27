<template>
  <section>
    <div class="container-lg">
      <div class="cta-info">
        <h1>Accurate and easy platform for productivity tracking</h1>
        <span
          >Our app help you to save time on tracking the activity, time,
          earnings, and more. Take everything under control with Baza.</span
        >

        <Button btn-type="primary" />
      </div>
      <div class="cta-img">
        <img src="../assets/6.png" alt="" srcset="" />
      </div>
    </div>
  </section>
</template>

<script>
import Button from "./widgets/Button.vue";

export default {
  name: "CTASection",
  components: {
    Button,
  },
};
</script>

<style lang="scss" scoped>
section {
  background-color: #fcfcfd;
  padding: 6rem 0 4rem 0;

  .container-lg {
    display: grid;
    grid-template-columns: repeat(auto-fill, 100%);

    @media screen and (min-width: 768px) {
      grid-template-columns: 1fr 700px;
    }

    .cta-info {
      margin: auto 0;
      padding-bottom: 3rem;

      h1 {
        font-size: 2.6rem;
        font-weight: 800;
        line-height: 150%;
      }

      span {
        display: block;
        margin-top: 1rem;
        font-size: 1.2rem;
        color: var(--text-body);
        line-height: 150%;
        margin-bottom: 4rem;
      }
    }

    .cta-img {
      @media screen and (max-width: 768px) {
        grid-row: 1;
      }

      img {
        max-width: 100%;
      }
    }
  }
}
</style>
