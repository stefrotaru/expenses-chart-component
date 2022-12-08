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
  props: {
    
  }
}
</script>

<style scoped>
.expensesApp {
  border: 1px solid white;
}
</style>
