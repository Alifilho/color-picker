<template>
    <div class="slider">
        <input type="range" min="0" max="255" :value="value" @input="$emit('rgb', $event.target.value)">
    </div>
</template>

<script>
export default {
    name: 'Slider',
    props: {
        value: Number,
    }
}
</script>

<style scoped>
</style>