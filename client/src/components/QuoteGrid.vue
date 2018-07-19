<template>
    <div class="row">
        <app-quote v-for="quote in quotes">{{ quotes }}</app-quote>
    </div>  
</template>

<script>
import Quote from './Quote.vue'
export default{
    props: ['quotes'],
    components:{
        appQuote: Quote
    }
}
</script>

<style>
</style>
