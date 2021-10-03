<template>
  <div>
    <p>Reaction time - {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </div>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = '🤯';
    } else if (this.score < 400) {
      this.rank = '😕';
    } else {
      this.rank = '❗';
    }
  },
};
</script>

<style scoped>
.rank {
  font-size: 1.4em;
  color: chocolate;
  font-weight: bold;
}
</style>
