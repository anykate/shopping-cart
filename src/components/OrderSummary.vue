<template>
    <div class="mx-auto mt-6 max-w-4xl flex-1 space-y-6 lg:mt-0 lg:w-full">
        <div
            class="space-y-4 rounded-lg border border-gray-200 bg-white p-4 shadow-sm sm:p-6 dark:border-gray-700 dark:bg-gray-800"
        >
            <p class="text-xl font-semibold text-gray-900 dark:text-white">
                Order summary
            </p>
            <a
                href="#"
                class="bg-primary-700 hover:bg-primary-800 focus:ring-primary-300 dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800 flex w-full items-center justify-center rounded-lg px-5 py-2.5 text-sm font-medium text-white focus:outline-none focus:ring-4"
                >Hide</a
            >

            <div class="space-y-4">
                <div class="space-y-2">
                    <dl class="flex items-center justify-between gap-4">
                        <dt
                            class="text-base font-normal text-gray-500 dark:text-gray-400"
                        >
                            Original price
                        </dt>
                        <dd
                            class="text-base font-medium text-gray-900 dark:text-white"
                        >
                            $7,592.00
                        </dd>
                    </dl>

                    <dl class="flex items-center justify-between gap-4">
                        <dt
                            class="text-base font-normal text-gray-500 dark:text-gray-400"
                        >
                            Savings
                        </dt>
                        <dd class="text-base font-medium text-green-600">
                            -$299.00
                        </dd>
                    </dl>

                    <dl class="flex items-center justify-between gap-4">
                        <dt
                            class="text-base font-normal text-gray-500 dark:text-gray-400"
                        >
                            Store Pickup
                        </dt>
                        <dd
                            class="text-base font-medium text-gray-900 dark:text-white"
                        >
                            $99
                        </dd>
                    </dl>

                    <dl class="flex items-center justify-between gap-4">
                        <dt
                            class="text-base font-normal text-gray-500 dark:text-gray-400"
                        >
                            Tax
                        </dt>
                        <dd
                            class="text-base font-medium text-gray-900 dark:text-white"
                        >
                            $799
                        </dd>
                    </dl>
                </div>

                <dl
                    class="flex items-center justify-between gap-4 border-t border-gray-200 pt-2 dark:border-gray-700"
                >
                    <dt
                        class="text-base font-bold text-gray-900 dark:text-white"
                    >
                        Total
                    </dt>
                    <dd
                        class="text-base font-bold text-gray-900 dark:text-white"
                    >
                        $8,191.00
                    </dd>
                </dl>
            </div>

            <a
                href="#"
                class="bg-primary-700 hover:bg-primary-800 focus:ring-primary-300 dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800 flex w-full items-center justify-center rounded-lg px-5 py-2.5 text-sm font-medium text-white focus:outline-none focus:ring-4"
                >Proceed to Checkout</a
            >
        </div>
    </div>
</template>

<script setup></script>

<style scoped></style>
