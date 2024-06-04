<template>
	<div class="mx-auto w-full flex-none lg:max-w-2xl xl:max-w-4xl">
		<CartListItem v-for="cartItem in cartItems" :key="cartItem.id" :item="cartItem"
			@remove-item="$emit('remove-item', $event)" />
	</div>
</template>

<script setup>
import CartListItem from '@/components/CartListItem.vue';
defineProps(['cartItems'])
defineEmits(['remove-item'])
</script>

<style scoped></style>
