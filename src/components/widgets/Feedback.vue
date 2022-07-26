<template>
    <div class="card-container">
        <div class="person-img" :style="'background-image: url(' + personImg + ')'">
        </div>

        <div class="person-body">
            <h1>"{{ personPhrase }}"</h1>
            <span>{{ personText }}</span>
            <h4>{{ personName }}</h4>
            <h5>{{ personRole }}</h5>
        </div>
    </div>
</template>

<script>
export default {
  name: "PersonItem",
  props: {
    personImg: String,
    personPhrase: String,
    personText: String,
    personName: String,
    personRole: String,
  }
};
</script>

<style lang="scss" scoped>
.card-container {
    padding: 3rem 0;

    .person-img {
        width: 100px;
        height: 100px;
        margin: auto;
        margin-bottom: 2rem;
        text-align: center;
        background-size: cover;
        background-position: center center;
        border-radius: 100px;
    }

    .person-body {
        text-align: center;

        h1 {
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        span {
            font-size: 1rem;
            margin: 2rem auto 1.2rem auto;
            display: block;
            color: var(--text-body);
            line-height: 150%;
            max-width: 40ch;
        }

        h4 {
            margin-bottom: 0.5rem;
            font-size: 1rem;

        }

        h5 {
            font-weight: 400;
            font-size: 1rem;
            color: var(--text-body);
        }
    }
}

</style>
