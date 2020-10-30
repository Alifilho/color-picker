<template>
  <div class="home">
    <Slider :value="rgb.r" @rgb="changeColor"/>
    <Slider :value="rgb.g" @rgb="changeColor"/>
    <Slider :value="rgb.b" @rgb="changeColor"/>

    <p>R: {{rgb.r}}</p>
    <p>G: {{rgb.g}}</p>
    <p>B: {{rgb.b}}</p>
  </div>
</template>

<script>
import Slider from '../components/elements/Slider'

export default {
  name: 'Home',
  components: {
    Slider
  },
  data: () => ({
    rgb: {
      r: 0,
      g: 123,
      b: 255
    }
  }),
  methods: {
    changeColor: function(color, position) {
      this.rgb[position] = color
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
