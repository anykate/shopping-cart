<template>
	<div>
		<CartTitle :username="username" />
		<div class="mt-6 sm:mt-8 md:gap-6 lg:flex lg:items-start xl:gap-8">
			<CartList :cart-items="shoppingCartItems" />
			<OrderSummary :cart-items="shoppingCartItems" />
		</div>
	</div>
</template>

<script setup>
import CartList from '@/components/CartList.vue'
import CartTitle from '@/components/CartTitle.vue'
import OrderSummary from '@/components/OrderSummary.vue'

import { ref } from 'vue'

let username = ref('Aniket')

let shoppingCartItems = ref([
	{
		id: 1,
		productName: 'Dragon Liver',
		price: 1500,
		isInStock: true,
		quantity: 3,
		image: 'src/assets/img/DragonLiver.png',
	},
	{
		id: 2,
		productName: 'Golden Snitch',
		price: 600,
		isInStock: true,
		quantity: 2,
		image: ' src/assets/img/GoldenSnitch.png',
	},
	{
		id: 3,
		productName: 'Unicorn Tail Hair',
		price: 1200,
		isInStock: false,
		quantity: 1,
		image: 'src/assets/img/UnicornTailHair.png',
	},
	{
		id: 4,
		productName: 'Wand',
		price: 2000,
		isInStock: true,
		quantity: 1,
		image: 'src/assets/img/Wand.jpg',
	},
	{
		id: 5,
		productName: 'Nimbus 2000',
		price: 5000,
		isInStock: true,
		quantity: 1,
		image: 'src/assets/img/Nimbus2000.jpg',
	},
])
</script>

<style scoped></style>
