<template>
	<div class="mx-auto mt-6 max-w-4xl flex-1 space-y-6 lg:mt-0 lg:w-full">
		<div
			class="space-y-4 rounded-lg border border-gray-200 bg-white p-4 shadow-sm sm:p-6 dark:border-gray-700 dark:bg-gray-800">
			<p class="text-xl font-semibold text-gray-900 dark:text-white">
				Order summary
			</p>
			<button
				class="bg-primary-700 hover:bg-primary-800 focus:ring-primary-300 dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800 flex w-full items-center justify-center rounded-lg px-5 py-2.5 text-sm font-medium text-white focus:outline-none focus:ring-4"
				@click="hideDetails = !hideDetails">
				{{ hideDetails ? 'Show Details' : 'Hide Details' }}
			</button>

			<div class="space-y-4">
				<div class="space-y-2" :class="{ 'hide-order-details': hideDetails }">
					<dl class="flex items-center justify-between gap-4">
						<dt class="text-base font-normal text-gray-500 dark:text-gray-400">
							Subtotal
						</dt>
						<dd class="text-base font-medium text-gray-900 dark:text-white">
							${{ subTotal }}
						</dd>
					</dl>

					<dl class="flex items-center justify-between gap-4">
						<dt class="text-base font-normal text-gray-500 dark:text-gray-400">
							Shipping Estimate
						</dt>
						<dd class="text-base font-medium text-green-600">
							${{ shippingEstimate }}
						</dd>
					</dl>

					<dl class="flex items-center justify-between gap-4">
						<dt class="text-base font-normal text-gray-500 dark:text-gray-400">
							Tax Estimate
						</dt>
						<dd class="text-base font-medium text-gray-900 dark:text-white">
							${{ taxEstimate }}
						</dd>
					</dl>

					<!-- <dl class="flex items-center justify-between gap-4">
						<dt class="text-base font-normal text-gray-500 dark:text-gray-400">
							Tax
						</dt>
						<dd class="text-base font-medium text-gray-900 dark:text-white">
							$799
						</dd>
					</dl> -->
				</div>

				<dl class="flex items-center justify-between gap-4 border-t border-gray-200 pt-2 dark:border-gray-700">
					<dt class="text-base font-bold text-gray-900 dark:text-white">
						Order Total
					</dt>
					<dd class="text-base font-bold text-gray-900 dark:text-white">
						${{ total }}
					</dd>
				</dl>
			</div>

			<a href="#"
				class="bg-primary-700 hover:bg-primary-800 focus:ring-primary-300 dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800 flex w-full items-center justify-center rounded-lg px-5 py-2.5 text-sm font-medium text-white focus:outline-none focus:ring-4">Proceed
				to Checkout</a>
		</div>
	</div>
</template>

<script setup>
import { ref, computed } from 'vue'

let hideDetails = ref(false)
const { cartItems } = defineProps(['cartItems'])

let subTotal = computed(() => cartItems.reduce((acc, item) => acc + item.price * item.quantity, 0))
let shippingEstimate = computed(() => subTotal.value > 10000 ? 100 : 50)
let taxEstimate = computed(() => subTotal.value * 0.08)
let total = computed(() => subTotal.value + shippingEstimate.value + taxEstimate.value)
</script>

<style scoped>
.hide-order-details {
	display: none;
}
</style>
