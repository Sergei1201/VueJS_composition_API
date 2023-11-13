<template>
  <Header />
  <div class="container">
  <Balance />
  <IncomeExpenses />
  <Transaction :transactions="transactions"/>
  <AddTransaction />
  </div>

</template>

<script setup>
import Header from './components/Header.vue'
import Balance from './components/Balance.vue'
import IncomeExpenses from './components/IncomeExpenses.vue'
import Transaction from './components/Transaction.vue'
import AddTransaction from './components/AddTransaction.vue'
// Making our state reactive by importing the ref hook from vue
import { ref } from 'vue'

const transactions = ref([
        {id: 1, text: 'Apples', amount: -30.5},
        {id: 2, text: 'Pears', amount: 45.6},
        {id: 3, text: 'Fruits', amount: -20.9},
        {id: 4, text: 'Vegetables', amount: -99.9}
    ])

// export default {
//   props: { 
//   },
//   components: {
//     Header,
//     Balance,
//     IncomeExpenses,
//     Transaction,
//     AddTransaction,
//   }
// }
</script>

<style>

</style>