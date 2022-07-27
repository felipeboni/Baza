<template>
  <div class="card">
    <div class="card-body">
      <span class="ribbon">{{ pricingName }}</span>

      <div class="price">
        <h1>{{ pricingValue }}$</h1>
        <span>monthly payment</span>
      </div>

      <ul>
        <li :class="[activeItems.includes(1) ? 'active' : '']">
          <font-awesome-icon
            icon="fa-solid fa-circle-check"
            size="lg"
            color="var(--secondary)"
          />
          <div class="text">
            <span>Time tracking</span>
          </div>
        </li>

        <li :class="[activeItems.includes(2) ? 'active' : '']">
          <font-awesome-icon
            icon="fa-solid fa-circle-check"
            size="lg"
            color="var(--secondary)"
          />
          <div class="text">
            <span>Activity monitoring</span>
          </div>
        </li>

        <li :class="[activeItems.includes(3) ? 'active' : '']">
          <font-awesome-icon
            icon="fa-solid fa-circle-check"
            size="lg"
            color="var(--secondary)"
          />
          <div class="text">
            <span>Generating reports</span>
          </div>
        </li>

        <li :class="[activeItems.includes(4) ? 'active' : '']">
          <font-awesome-icon
            icon="fa-solid fa-circle-check"
            size="lg"
            color="var(--secondary)"
          />
          <div class="text">
            <span>Company analytics</span>
          </div>
        </li>
      </ul>

      <Button btn-type="primary" :btn-link="CTAUrl" />
    </div>
  </div>
</template>

<script>
import { library } from "@fortawesome/fontawesome-svg-core";
import { faCircleCheck } from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

library.add(faCircleCheck);

import Button from "./Button.vue";

export default {
  name: "PricingItem",
  props: {
    pricingValue: String,
    pricingName: String,
    activeItems: Array,
    CTAUrl: String,
  },
  components: {
    "font-awesome-icon": FontAwesomeIcon,
    Button,
  },
};
</script>

<style lang="scss" scoped>
.card {
  background-color: var(--background);
  padding: 2rem;
  border-radius: 1.8rem;
  text-align: center;

  .card-body {
    .ribbon {
      background-color: var(--primary-light);
      color: var(--primary);
      font-weight: 700;
      letter-spacing: 2px;
      font-size: 0.875rem;
      padding: 0.2rem calc(0.875rem - 0.2em) 0.2rem 0.875rem;
      border-radius: 0.3rem;
      display: inline-block;
      margin-bottom: 1.4rem;
      text-transform: uppercase;
    }

    .price {
      h1 {
        font-size: 3.2rem;
        font-weight: 800;
        margin-bottom: 0.6rem;
      }

      span {
        font-weight: 700;
        color: var(--primary);
      }
    }

    ul {
      list-style: none;
      margin: 2rem 0;

      li {
        display: flex;
        align-items: center;
        gap: 1rem;
        opacity: 0.5;

        &.active {
          opacity: 1;
        }

        span {
          color: var(--text-body);
          font-weight: 700;
        }
      }

      li + li {
        margin-top: 1.4rem;
      }
    }
  }
}

/deep/ .btn {
  margin: 0 auto;
}
</style>
