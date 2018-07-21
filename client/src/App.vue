<template>
    <div class="container">
        <app-New-Quote @newQuoteAdded="newQuote"></app-New-Quote>
        <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'
export default{
    data: function(){
        return{
            quotes:['This is a test Quote'], 
            maxQuotes: 10
        }
    },
    methods:{
        newQuote(quote){
            this.quotes.push(quote)
        }
    },
    components:{
        appQuoteGrid: QuoteGrid,
        appNewQuote: NewQuote
    }
}

</script>

<style>
</style>
