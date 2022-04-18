<template>
   <hr> <h2>Reusability with Mixins</h2>
    <div>
        <h3 @mouseover="increaseCount"> Hovered Amount = {{count}}</h3>
    </div>
</template>

<script>
import CounterMixin from '../components/counterMixin';
    export default {
        name : "Hovered-Amount",
        mixins : [CounterMixin],

    }
</script>

<style scoped>

</style>