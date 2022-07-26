<template>
  <div class="tile-img">
    <img :src="tileImg" />
  </div>

  <div class="tile-body">
    <h1>{{ tileTitle }}</h1>
    <span>{{ tileText }}</span
    >
  </div>
</template>

<script>
export default {
  name: "TileItem",
  props: {
    tileImg: String,
    tileTitle: String,
    tileText: String,
  }
};
</script>

<style lang="scss" scoped>
.tile-img {
    margin-bottom: 1rem;

    img {
        max-width: 75px;
        width: 100%;
    }
}

.tile-body {
    h1 {
        margin-bottom: 1rem;
    }

    span {
        line-height: 150%;
        color: var(--secondary);
        letter-spacing: 0.5px;
    }
}
</style>
