<template>
  <div class="card">
    <div class="card-body">

      <span class="ribbon">LITE</span>

      <div class="price">
        <h1>10$</h1>
        <span>monthly payment</span>
      </div>

      <ul>
        <li>
            <font-awesome-icon icon="fa-solid fa-circle-check" size="lg" color="var(--secondary)"/>
            <div class="text">
              <h2>Create tasks</h2>
            </div>
        </li>
      </ul>

      <Button btn-type="primary" />

    </div>
  </div>
</template>

<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { faCircleCheck } from '@fortawesome/free-solid-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

library.add(faCircleCheck);

import Button from './Button.vue'

export default {
  name: "PricingItem",
  components:  {
    'font-awesome-icon': FontAwesomeIcon,
    Button
  },
};
</script>

<style lang="scss" scoped>
.card {
  background-color: var(--background);
  padding: 2rem;
  border-radius: 1.8rem;
  text-align: center;

  .ribbon {
    background-color: var(--primary-light);
    color: var(--primary);
    font-weight: 700;
    letter-spacing: 3px;
    font-size: 0.875rem;
    padding: 0.2rem calc(0.875rem - 0.3em) 0.2rem 0.875rem;
    border-radius: 0.3rem;
  }

  h1 {
    font-size: 3rem;
  }
}
</style>
