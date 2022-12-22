<template>
  <div>
    <h4>Your reaction time was</h4>
    <p>{{ score }}ms</p>
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
      this.rank = 'Ninja fingers';
    } else if (this.score < 400) {
      this.rank = 'Rapid Reflexes';
    } else {
      this.rank = 'Slow poke';
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
