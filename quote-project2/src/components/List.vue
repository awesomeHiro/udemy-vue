<template>
    <div class="container">
        <h1>list</h1>
        <ul id="example-1">
            <li v-for="quote in quotes" :key="quote">
                {{ quote }}
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        data: function(){
            return {
                quotes: [
                    'Quote1',
                    'Quote2',
                    'Quote3',
                    'Quote4',
                    'Quote5',
                    'Quote6',
                    'Quote7',
                    'Quote8',
                    'Quote9',
                    'Quote10',
                ]
            }
        }
    }
</script>

<style>
</style>
