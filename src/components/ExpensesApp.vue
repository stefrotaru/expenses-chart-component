<template>
  <div class="expensesApp">
    <ExpensesHeader/>
    <ExpensesMain/>
  </div>
</template>

<script>
import ExpensesHeader from './ExpensesHeader.vue';
import ExpensesMain from './ExpensesMain.vue';

export default {
  name: 'ExpensesApp',
  components: {
    ExpensesHeader,
    ExpensesMain,
  },
}
</script>

<style scoped>
</style>
