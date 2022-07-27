<template>
  <section>
    <div class="container">
      <ul>
        <li>
          <h1><count-up duration="5" :end-val="90" :options="{suffix: 'K'}"></count-up></h1>
          <span>Active users</span>
        </li>
        <li>
          <h1><count-up duration="5" :end-val="62" :options="{suffix: 'M+'}"></count-up></h1>
          <span>Tasks completed</span>
        </li>
        <li>
          <h1><count-up duration="5" :end-val="68" :options="{suffix: 'K'}"></count-up></h1>
          <span>Reports generated</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import CountUp from 'vue-countup-v3'

export default {
  name: "StatsSection",
  components: {
    'count-up': CountUp
  }
};
</script>

<style lang="scss" scoped>
section {
    border-bottom: 1px solid rgba(0,0,0,0.1);

  .container {
    margin: auto;
    padding: 4rem 0;

    ul {
      display: grid;
      grid-template-columns: repeat(auto-fill, 333px);
      gap: 5rem;
      justify-content: center;
      
      list-style: none;

      li {
        text-align: center;

        h1 {
          font-size: 3rem;
          font-weight: 800;
          margin-bottom: 1rem;
        }

        span {
          color: var(--text-body);
        }
      }
    }
  }
}
</style>
