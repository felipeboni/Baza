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
            <Pricing pricing-value="10" pricing-name="lite" cta-url="#" :active-items=[1,2] />
          </li>
          <li>
            <Pricing pricing-value="30" pricing-name="pro" cta-url="#" :active-items=[1,2,3] />
          </li>
          <li>
            <Pricing pricing-value="80" pricing-name="business" cta-url="#" :active-items=[1,2,3,4] />
          </li>
        </ul>
      </div>

      <div class="faq">
        <ul>

          <li>
            <font-awesome-icon icon="fa-solid fa-circle-question" size="2xl" color="var(--text-accent)"/>
            <div class="text">
              <h2>Install the app</h2>
              <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
            </div>
          </li>

          <li>
            <font-awesome-icon icon="fa-solid fa-circle-question" size="2xl" color="var(--text-accent)"/>
            <div class="text">
              <h2>Set the goals</h2>
              <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
            </div>
          </li>

          <li>
            <font-awesome-icon icon="fa-solid fa-circle-question" size="2xl" color="var(--text-accent)"/>
            <div class="text">
              <h2>Create tasks</h2>
              <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
            </div>
          </li>

          <li>
            <font-awesome-icon icon="fa-solid fa-circle-question" size="2xl" color="var(--text-accent)"/>
            <div class="text">
              <h2>Install the app</h2>
              <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
            </div>
          </li>

          <li>
            <font-awesome-icon icon="fa-solid fa-circle-question" size="2xl" color="var(--text-accent)"/>
            <div class="text">
              <h2>Set the goals</h2>
              <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
            </div>
          </li>

          <li>
            <font-awesome-icon icon="fa-solid fa-circle-question" size="2xl" color="var(--text-accent)"/>
            <div class="text">
              <h2>Create tasks</h2>
              <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
            </div>
          </li>

        </ul>
      </div>

      <div class="help">
        <span>Didn't find your answer?<a href="#">&nbsp; Contact us now</a></span>
      </div>

    </div>

  </section>
</template>

<script>
import Pricing from './widgets/Pricing.vue'

import { library } from '@fortawesome/fontawesome-svg-core'
import { faCircleQuestion } from '@fortawesome/free-solid-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

library.add(faCircleQuestion);

export default {
  name: "PricingTableSection",
  components:  {
    'font-awesome-icon': FontAwesomeIcon,
    Pricing
  },
};
</script>


<style lang="scss" scoped>

section {
  background: var(--dark);
  padding: 5rem 0;

  .container {
    margin: 0 auto;

    .headline {
      margin: 0 auto;
      padding-bottom: 1rem;
      text-align: center;
      max-width: 63ch;
      color: #fff;

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
      }
    }

    .pricing-table {
        ul {
          list-style: none;
          display: grid;
          gap: 3rem;
          grid-template-columns: repeat(auto-fill, 340px);
          justify-content: center;
        }
    }

    .faq {
      color: #fff;

      ul {
        display: grid;
        grid-template-columns: repeat(auto-fill, 100%);
        justify-content: center;
        margin-top: 8rem;

        @media screen and (min-width: 768px) {
          grid-template-columns: repeat(auto-fill, 560px);
        }

        li {
          display: flex;
          gap: 1.2rem;
          max-width: 55ch;
          margin-bottom: 4rem;

          h2 {
            margin-bottom: 0.5rem;
          }

          span {
            line-height: 150%;
            opacity: 0.5;
          } 
        }
      }
    }

    .help {
      color: #fff;
      text-align: center;
      margin-top: 1rem;
      margin-bottom: 2rem;
      font-size: 1.2rem;

      a {
        color: var(--text-accent);
        position: relative;

        &::before {
          content: '';
          position: absolute;
          width: calc(100% - .5em);
          height: 2px;
          left: .5em;
          bottom: -5px;
          background-color: var(--text-accent);

          transform-origin: center;
          transform: scaleX(0);

          transition: transform 0.2s;
        }

        &:hover {
          &::before {
            transform: scaleX(1);
          }
        }

      }
    }
  }
}
</style>
