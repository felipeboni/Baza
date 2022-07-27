<template>
  <section>
    <div class="container">
      <ul>
        <li>
          <Tile tile-img="./img/4.png" tile-title="Time tracking" tile-text="Our app will help you to save time on tracking the activity, time, earnings and more. Any time you can be sure everything is under your control." />
        </li>
        <li>
          <Tile tile-img="./img/5.png" tile-title="Activity Monitoring" tile-text="Our app will help you to save time on tracking the activity, time, earnings and more. Any time you can be sure everything is under your control." />
        </li>
        <li>
          <Tile tile-img="./img/10.png" tile-title="Generating Reports" tile-text="Our app will help you to save time on tracking the activity, time, earnings and more. Any time you can be sure everything is under your control." />
        </li>
      </ul>
    </div>

  </section>
</template>

<script>
import Tile from './widgets/Tile.vue'

export default {
  name: 'TilesSection',
  components: {
    Tile
  }
}
</script>


<style lang="scss" scoped>
.container {
  margin: 8.5rem auto;

  ul {
    display: grid;
    grid-template-columns: repeat(auto-fill, 320px);
    gap: 5rem;
    justify-content: center;

    list-style: none;
  }
}
</style>
