<template>
    <div class="slider">
        <input type="range" min="0" max="255" v-model="value">
    </div>
</template>

<script>


export default {
    name: 'Slider',
    props: {
        propValue: Number,
    },
    created() {
        this.value = this.propValue
    },
    data: () => ({
        value: 0
    }),
    watch: {
        value() {
            this.$emit('rgb', this.value)
        }
    }
    
}
</script>

<style scoped>
    .slider {
        
    }
</style>