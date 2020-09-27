<template>
  <div class="key">
    <img :src="imagePath" :style="rotationStyle" @mouseOver="onMouseOver()"/>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    number: String
  },
  computed: {
    rotationStyle() {
      const degreeMatrix = [0,0, 0, 90, -90, 0, 90, -90, 180, 180];
      const rotationDegree = degreeMatrix[this.number];

      return `transform: rotate(${rotationDegree}deg)`; 
    },
    imagePath() {
      return require(`../assets/keys/cropped-${this.number%2}.png`);
    }
  },
  methods: {
    onMouseOver() {
      const notePath = require(`../assets/samples/key-${this.number}.mp3`);
      const note = new Audio(notePath);
      note.play();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
