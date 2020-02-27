<template lang="html">
    <div id="events">
        <button type="button" name="button" v-on:click="msg">button</button>
    </div>
</template>

<script>
export default {
        methods: {
            msg: function () {
                   window.console.log(Math.random())
            }
        }
    }
</script>

<style lang="css">

</style>
