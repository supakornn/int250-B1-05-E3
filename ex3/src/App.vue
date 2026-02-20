<script setup>
import PricingCard from "./components/PricingCard.vue";

const plans = [
    {
        name: "Basic",
        storage: "100GB",
        price: "$1.99",
        featured: false,
        features: [
            "100 GB storage",
            "Option to add members",
            "Extra member benefits",
        ],
    },
    {
        name: "Standard",
        storage: "200GB",
        price: "$3.99",
        featured: true,
        features: [
            "200 GB storage",
            "Option to add members",
            "Extra member benefits",
        ],
    },
    {
        name: "Premium",
        storage: "2TB",
        price: "$8.99",
        featured: false,
        features: [
            "2 TB storage",
            "Option to add members",
            "Extra member benefits",
        ],
    },
];
</script>

<template>
    <main
        class="min-h-screen bg-[#13132a] flex items-center justify-center px-6"
    >
        <div class="flex flex-wrap items-center justify-center gap-6">
            <PricingCard v-for="plan in plans" :key="plan.name" :plan="plan" />
        </div>
    </main>
</template>
