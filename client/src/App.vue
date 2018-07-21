<template>
    <div class="container">
        <app-New-Quote @newQuoteAdded="newQuote"></app-New-Quote>
        <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
        <div class="row">
            <div class="alert alert-info">Alert: Click on a quote to delete it!</div>
        </div>
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
        },
        deleteQuote(index){
            this.quotes.splice(index, 1)
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
