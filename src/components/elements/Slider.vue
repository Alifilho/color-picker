<template>
    <div class="slider">
        <input type="range" min="0" max="255" :value="value[1]" @input="$emit('rgb', Number($event.target.value), value[0])">
    </div>
</template>

<script>
export default {
    name: 'Slider',
    props: {
        value: Array,
    }
}
</script>

<style scoped>
</style>