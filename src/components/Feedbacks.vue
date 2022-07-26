<template>
  <section>
    <div class="container">
      <ul>
        <li>
          <Feedback
            person-img="./img/9.png"
            person-phrase="Best choice!"
            person-text="Easy to install the app, no specific skills needed. Take everything under control with Baza."
            person-name="Mat Goldman"
            person-role="Developer"
          />
        </li>
        <li>
          <div class="dotted-line"></div>
        </li>
        <li>
          <Feedback
            person-img="./img/8.png"
            person-phrase="Happy CEO, happy team"
            person-text="I am happy that I chose Baza to work with my remote team."
            person-name="Max Smit"
            person-role="CEO of Fast Tech"
          />
        </li>
      </ul>
    </div>

  </section>
</template>

<script>
import Feedback from './widgets/Feedback.vue'

export default {
  name: 'FeedbacksSection',
  components: {
    Feedback,
  }
}
</script>


<style lang="scss" scoped>
section {
  background-color: #fcfcfd;
  padding: 5rem 0;

  .container {
    ul {
      display: grid;
      grid-template-columns: 1fr 1px 1fr;
      gap: 5rem;
      list-style: none;

      .dotted-line {
        height: 100%;
        border-left: 1px dashed rgba(0, 0, 0, 0.1);
      }
    }
  }
}

</style>
