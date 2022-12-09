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
.spendings__left-col > p {
    padding-block-end: .25rem;
    color: hsl(28, 10%, 53%);
}
.spendings__right-col {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
}
.spendings__right-col > p {
    padding-block-start: .25rem;
}
.spendings__percentage {
    font-size: 1.2rem;
    font-weight: 600;
    align-self: flex-end;
    justify-self: flex-end;
}
.spendings__total {
    font-size: 2.5rem;
    font-weight: 600;
}
</style>