<template>
    <div class="container">
        <cheader></cheader>
        <hr>
        <cadd></cadd>
        <hr>
        <clist></clist>
        <hr>
        <cfooter></cfooter>
    </div>
</template>

<script>
import cheader from "./components/Header.vue"
import cadd from "./components/Add.vue"
import clist from "./components/List.vue"
import cfooter from "./components/Footer.vue"
    export default {
        components: {
            cheader,
            cadd,
            clist,
            cfooter
        }
    }
</script>

<style>
</style>
