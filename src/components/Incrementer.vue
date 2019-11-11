<template>
    <div class="incrementer">
        <p>{{ countString }}</p>
        <button @click="increment">Increment!</button>
        <button @click="decrement">Decrement!</button>
    </div>    
</template>

<script>
    export default {
        props: {
            count: Number,
        },
        computed: {
            countString() {
                return `The count is ${this.count}`
            }
        },
        methods: {
            increment() {
                this.$emit("increment", 1)
            },
            decrement() {
                this.$emit("decrement", 1)
            }
        }
    }
</script>

<style lang="scss">

</style>