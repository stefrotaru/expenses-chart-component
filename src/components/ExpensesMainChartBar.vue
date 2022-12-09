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
                '--chartBar-hover-content': `'$${this.expenses.amount}'`,
                '--chartBar-height': `${this.expenses.amount * 2}px`,
            }
        }
    },
    created () {}
}
</script>

<style scoped>
.chartBar {
    display: flex;
    flex-direction: column;
    position: relative;
}
.chartBar__procentage {
    background-color: hsl(10, 79%, 65%);
    border-radius: 5px;
    width: 2.5rem;
    height: var(--chartBar-height);
}
.chartBar__procentage:hover {
    opacity: 0.7;
    cursor: pointer;
}
.chartBar__procentage:hover::after {
    content: var(--chartBar-hover-content);
    background-color: hsl(25, 47%, 15%);
    color: hsl(33, 100%, 98%);
    border-radius: 5px;
    font-size: .80rem;
    padding: .5rem;
    position: absolute;
    top: -3em;
    right: -.5em;
}
.chartBar__label {
    padding-block-start: .5rem;
    align-self: center;
}

@media (max-width: 450px) {
    .chartBar__procentage {
        background-color: hsl(10, 79%, 65%);
        border-radius: 5px;
        width: 2rem;
        height: var(--chartBar-height);
    }

    .chartBar__procentage:hover::after {
        content: var(--chartBar-hover-content);
        background-color: hsl(25, 47%, 15%);
        color: hsl(33, 100%, 98%);
        border-radius: 5px;
        font-size: .80rem;
        padding: .5rem;
        position: absolute;
        top: -3.5em;
        right: -1em;
    }
}
</style>