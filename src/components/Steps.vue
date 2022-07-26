<template>
  <section>
    <div class="container">
      <div class="headline">
        <h1>Improve team productivity</h1>
        <span
          >Our app help you to save time on tracking the activity, time,
          earnings, and more. Take everything under control with Baza.</span
        >
      </div>
      <div class="inner-container">
        <div class="stats-img">
          <img src="../assets/7.png" alt="" srcset="" />
        </div>

        <div class="stats-info">
          <ul>
            <li>
              <font-awesome-icon icon="fa-solid fa-circle-check" size="2xl" color="var(--primary)"/>
              <div class="text">
                <h2>Install the app</h2>
                <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
              </div>
            </li>
            <li>
              <font-awesome-icon icon="fa-solid fa-circle-check" size="2xl" color="var(--primary)"/>
              <div class="text">
                <h2>Set the goals</h2>
                <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
              </div>
            </li>
            <li>
              <font-awesome-icon icon="fa-solid fa-circle-check" size="2xl" color="var(--primary)"/>
              <div class="text">
                <h2>Create tasks</h2>
                <span>Easy to install the app, no specific skills needed. Take everything under control with Baza.</span>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { faCircleCheck } from '@fortawesome/free-solid-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

library.add(faCircleCheck);

export default {
  name: "StepsSection",
  components:  {
    'font-awesome-icon': FontAwesomeIcon
  },
};
</script>

<style lang="scss" scoped>
.container {
  max-width: 1300px;
  margin: 0 auto;
  padding: 5rem 0;

  .headline {
    margin: auto;
    padding-bottom: 1rem;
    text-align: center;
    max-width: 63ch;

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

  .inner-container {
    padding: 0 20px;
    display: grid;
    align-items: center;
    grid-template-columns: 1fr 1fr;
    gap: 1.3rem;

    .stats-img {
      img {
        max-width: 100%;
      }
    }

    .stats-info {
      ul {
        list-style: none;

        li {
          display: flex;
          gap: 1.2rem;

          h2 {
            margin-bottom: 0.875rem;
          }

          span {
            color: var(--text-body);
            line-height: 150%;
          } 
        }

        li + li {
          margin-top: 3rem;
        }
      }
    }
  }
}
</style>
