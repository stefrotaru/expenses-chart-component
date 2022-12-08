<template>
    <div class="expenses">
        <ExpensesMainChart/>
        <hr>
        <ExpensesMainSpendings :totalSpendingsMonth="totalSpendingsMonth" :spendingsProcLastMonth="spendingsProcLastMonth"/>
    </div>
</template>

<script>
import ExpensesMainChart from './ExpensesMainChart.vue';
import ExpensesMainSpendings from './ExpensesMainSpendings.vue';

export default {
    name: 'ExpensesMain',
    data () {
        return {
            totalSpendingsMonth: 478.33,
            spendingsProcLastMonth: 2.4,
        }
    },
    components: {
        ExpensesMainChart,
        ExpensesMainSpendings,
    }
}
</script>

<style>
.expenses {
    display: flex;
    flex-direction: column;
}

.expenses > hr {
    width: 87.5%;
    align-self: center;
}
</style>