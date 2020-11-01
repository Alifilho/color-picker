<template>
  <div class="home">
    <ColorDisplay :rgba="rgba"/>

    <Slider :value="rgba.r" @rgb="changeColor"/>
    <Slider :value="rgba.g" @rgb="changeColor"/>
    <Slider :value="rgba.b" @rgb="changeColor"/>
    <Slider :value="rgba.a" @rgb="changeColor" />

    <p>R: {{rgba.r[1]}}</p>
    <p>G: {{rgba.g[1]}}</p>
    <p>B: {{rgba.b[1]}}</p>
    <p>A: {{rgba.a[1]}}</p>
  </div>
</template>

<script>
import Slider from '../components/elements/Slider'
import ColorDisplay from '../components/elements/ColorDisplay'

export default {
  name: 'Home',
  components: {
    Slider,
    ColorDisplay
  },
  data: function() {
    return {
      rgba: {
      r: ['r', 0],
      g: ['g', 123],
      b: ['b', 255],
      a: ['a', 0]
      }
    }
  },
  methods: {
    changeColor: function(color, position) {
      this.$set(this.rgba[position], 1, color)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
