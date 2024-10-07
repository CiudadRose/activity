<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { ref } from 'vue'; // Import ref for reactive state

// Create a reactive count variable
const count = ref(0);

// Method to increment the count
const increment = () => {
    count.value++;
};

// Method to decrement the count
const decrement = () => {
    count.value--;
};
</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Dashboard
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <div class="p-6 flex flex-col items-center"> <!-- Centering the content -->
                        <h1 class="text-2xl font-bold">Activity 1</h1>
                        <p class="text-lg mt-4">{{ count }}</p> <!-- Display current count only -->
                        <div class="mt-4 flex space-x-4"> <!-- Flexbox for button spacing -->
                            <button @click="increment" class="bg-blue-500 text-white px-4 py-2 rounded">Increment</button>
                            <button @click="decrement" class="bg-red-500 text-white px-4 py-2 rounded">Decrement</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </AppLayout>
</template>
