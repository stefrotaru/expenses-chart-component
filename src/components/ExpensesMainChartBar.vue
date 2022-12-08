<template>
    <div class="chartBar" id="chartBar">
        <div class="chartBar__procentage" :style="cssProps" ></div>
        <label class="chartBar__label" for="chartBar">{{expenses.day}}</label>
    </div>
</template>

<script>
export default {
    name: 'ExpensesMainChartBar',
    data () {
        return {
            
        }
    },
    props: ['expenses'],
    methods: {},
    computed: {
        cssProps() {
            return {
                '--chartBar-height': `${this.expenses.amount * 2}px`,
            }
        }
    },
    created () {

    }
}
</script>

<style scoped>
.chartBar {
    
    display: flex;
    flex-direction: column;
}
.chartBar__procentage {
    background-color: blue;
    border-radius: 5px;
    width: 3rem;
    height: var(--chartBar-height);
}
.chartBar__label {
    align-self: center;
}
</style>