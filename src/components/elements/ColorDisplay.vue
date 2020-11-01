<template>
    <div class="color-display" :style="cssProps"></div>
</template>

<script>
export default {
    name: 'ColorDisplay',
    props: {
        rgba: Object
    },
    data: function() {
        return {
            background: `${this.rgba.r[1]}, ${this.rgba.g[1]}, ${this.rgba.b[1]}, ${this.rgba.a[1]}`
        }
    },
    created: function() {
        console.log(this.rgba)
    },
    computed: {
        cssProps() {
            return {
                '--background': this.background
            }
        }
    }
}
</script>

<style scoped>
.color-display {
    width: 250px;
    height: 250px;
    background-color: red;
    margin-bottom: 20px;
    background-color: rgba(var(--background));
}
</style>