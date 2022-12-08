<template>
    <div class="header">
        <div class="header__myBalance">
            <p class="header__myBalance-title">My balance</p>
            <span class="header__myBalance-money">$921.48</span>
        </div>
        <div class="header__logo">
            <img src="../assets/logo.svg" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'ExpensesHeader',

}
</script>

<style scoped>
.header {
    border: 1px solid white;
    /* max-width: 500px; */
    padding: 1rem;

    display: flex;
    justify-content: space-between;
    /* gap: 1rem; */
}
.header__myBalance {
    
}
.header__myBalance-title {
    font-size: .8rem;
    padding-bottom: .5rem;
}
.header__myBalance-money {
    font-size: 1.5rem;
}
.header__logo {}
</style>