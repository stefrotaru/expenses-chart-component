<template>
    <div class="chart-container">
        <h1 class="chart-title">Spending - Last 7 days</h1>
        <div class="chart">
            <ExpensesMainChartBar v-for="(day, index) in weekExpenses" v-bind:key="day" v-bind:expenses="weekExpenses[index]"/>
        </div>
    </div>
</template>

<script>
import ExpensesMainChartBar from './ExpensesMainChartBar.vue';
import Json from '../../data.json';

export default {
    name: 'ExpensesMainChart',
    data () {
        return {
            weekExpenses: Json,
            totalExpensesWeek: this.calcTotalExpenses(),
        }
    },
    methods: {
        calcTotalExpenses() {
            let total = 0;
            for (var i = 0; i < Json.length; i++) {
                total += Json[i].amount;
            }
            return total;
        }
    },
    components: {
        ExpensesMainChartBar
    },
    created () {
        
    },
}
</script>

<style >
.chart-container {
    padding: 2rem;
}
.chart-title {
    padding-bottom: 4rem;
}
.chart {
    /* padding: 2rem; */

    display: flex;
    align-items: baseline;
    gap: 1rem;
}

.chart > .chartBar:nth-child(3) > .chartBar__procentage {
    background-color: hsl(186, 34%, 60%);
}
</style>