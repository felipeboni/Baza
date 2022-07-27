<template>
  <section>
    <div class="container-lg">
      <div class="inner-container">
        <div class="text">
          <img
            class="img-left"
            src="../assets/2.png"
            alt="Man touching a lamp"
          />

          <h1>Ready to improve productivity?</h1>

          <span
            >Our app help you to save time on tracking the activity, time,
            earnings, and more. Take everything under control with Baza.</span
          >
        </div>

        <div class="btn-left">
          <Button btn-type="primary" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Button from "./widgets/Button.vue";

export default {
  name: "FooterCTASection",
  components: {
    Button,
  },
};
</script>

<style lang="scss" scoped>
.container-lg {
  padding-top: 5rem;
  position: relative;

  .inner-container {
    text-align: left;
    display: grid;
    gap: 7rem;
    margin-left: auto;
    width: fit-content;
    grid-template-columns: 600px 250px;
    align-items: center;

    .text {
      position: relative;
      margin: 0 auto;

      .img-left {
        position: absolute;
        width: 100%;
        max-width: 270px;
        left: -47%;
        top: -82%;
      }

      h1 {
        font-size: 2.6rem;
        font-weight: 800;
        line-height: 150%;
        margin-bottom: 1rem;
      }

      span {
        display: block;
        font-size: 1.2rem;
        line-height: 150%;
        margin-bottom: 3rem;
        max-width: 55ch;
        color: var(--text-body);
      }
    }
  }
}
</style>
