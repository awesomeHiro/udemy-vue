<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12"> 
                <button @click="selectedComp = 'compAuthor'">Author</button>
                <button @click="selectedComp = 'compNew'">New</button>
                <button @click="selectedComp = 'compQuote'">Quote</button>
                <h2>{{ selectedComp }}</h2>
                <component :is="selectedComp"></component>
                <hr>
                <h2>A wonderful quote</h2>
            </div>
        </div>
    </div>
</template>

<script>
    import compQuote from './components/Quote.vue'
    import compAuthor from './components/Author.vue'
    import compNew from './components/New.vue'
    export default {
        data: function(){
                return {
                    quoteTitle: 'Quote',
                    selectedComp: 'compNew'
                }
        },
        components:{
            compQuote,
            compAuthor,
            compNew
        } 
    }
</script>

<style>
</style>
