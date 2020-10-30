<template>
  <div class="home">
    <Slider :value="r" @rgb="changeColor"/>
    <Slider :value="g" @rgb="changeColor"/>
    <Slider :value="b" @rgb="changeColor"/>

    <p>R: {{r}}</p>
    <p>G: {{g}}</p>
    <p>B: {{b}}</p>
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
    r: 125,
    g: 0,
    b: 255
  }),
  methods: {
    changeColor: (color) => {
      this.r = color;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
