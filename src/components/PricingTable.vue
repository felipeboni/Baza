<template>
  <section>
    <div class="container">

      <div class="headline">
        <h1>Our Pricing</h1>
        <span
          >Our app help you to save time on tracking the activity, time,
          earnings, and more. Take everything under control with Baza.</span
        >
      </div>

      <div class="pricing-table">
        <ul>
          <li>
            <Pricing tile-img="./img/4.png" tile-title="Time tracking" tile-text="Our app will help you to save time on tracking the activity, time, earnings and more. Any time you can be sure everything is under your control." />
          </li>
        </ul>
      </div>

    </div>

  </section>
</template>

<script>
import Pricing from './widgets/Pricing.vue'

export default {
  name: 'PricingTableSection',
  components: {
    Pricing
  }
}
</script>


<style lang="scss" scoped>

section {
  background: var(--dark);
}

.container {
  margin: 8.5rem auto;

  .headline {
    margin: auto;
    padding-bottom: 1rem;
    text-align: center;
    max-width: 63ch;
    color: #fff;

    h1 {
      font-size: 2.6rem;
      font-weight: 800;
      line-height: 150%;
    }

    span {
      display: block;
      margin-top: 1rem;
      font-size: 1.2rem;
      line-height: 150%;
      margin-bottom: 4rem;
    }
  }

  ul {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 5rem;

    list-style: none;
  }
}
</style>
