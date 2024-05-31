<template>
    <div>
        <CartTitle />
        <div class="mt-6 sm:mt-8 md:gap-6 lg:flex lg:items-start xl:gap-8">
            <CartList />
            <OrderSummary />
        </div>
    </div>
</template>

<script setup>
import CartList from '@/components/CartList.vue';
import CartTitle from '@/components/CartTitle.vue';
import OrderSummary from '@/components/OrderSummary.vue';
</script>

<style scoped></style>
