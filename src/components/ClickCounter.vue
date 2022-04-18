<template>
    <div>
        <button @click="increaseCount">Click Counter = {{count}}</button>
    </div>
</template>

<script>
import CounterMixin from '../components/counterMixin';
    export default {
        name : "Click-Amount",
        mixins : [CounterMixin],

    }
</script>

<style scoped>

</style>