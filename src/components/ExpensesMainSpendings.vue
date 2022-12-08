<template>
    <div class="spendings">
        <div class="spendings__left-col">
            <p>Total this month</p>
            <span class="spendings__total">${{totalSpendingsMonth}}</span>
        </div>
        <div class="spendings__right-col">
            <span class="spendings__percentage">+{{spendingsProcLastMonth}}%</span>
            <p>from last month</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ExpensesMainSpendings',
    props: ['totalSpendingsMonth', 'spendingsProcLastMonth']
}
</script>

<style>
.spendings {
    padding: 2rem;

    display: flex;
    justify-content: space-between;
}

.spendings__right-col {
    display: flex;
    flex-direction: column;
}
.spendings__percentage {
    align-self: flex-end;
}
</style>