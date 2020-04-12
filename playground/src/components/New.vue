<template>
    <div>
        <h3>New</h3>
        <p>{{conunter}}</p>
        <button @click="conunter++">INCREASE!</button>
    </div>
</template>

<script>
    export default {
        data:function(){
            return {
                conunter: 0
            }
        }
    }
</script>

<style>
</style>
