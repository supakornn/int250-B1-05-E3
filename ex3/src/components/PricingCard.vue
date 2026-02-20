<script setup>
import PricingFeatureList from "./PricingFeatureList.vue";

const props = defineProps({
    plan: {
        type: Object,
        required: true,
    },
});
</script>

<template>
    <div
        class="flex flex-col rounded-2xl overflow-hidden w-72"
        :class="[
            plan.featured
                ? 'ring-4 ring-purple-500 bg-[#1a1a2e]'
                : 'ring-1 ring-[#3a3a50] bg-[#1e1e30]',
        ]"
    >
        <!-- Top section -->
        <div class="flex flex-col items-center px-8 pt-10 pb-8 gap-4">
            <span class="text-xs tracking-[0.2em] uppercase text-gray-300">
                {{ plan.name }}
            </span>

            <div class="text-center">
                <p class="text-6xl text-white font-serif">
                    {{ plan.storage }}
                </p>
                <p class="text-gray-400 mt-1">{{ plan.price }}/month</p>
            </div>

            <button
                class="mt-2 w-full py-3 rounded-lg font-medium transition-colors duration-200"
                :class="[
                    plan.featured
                        ? 'bg-purple-600 hover:bg-purple-700 text-white'
                        : 'bg-transparent border border-purple-500 hover:bg-purple-600 text-white',
                ]"
            >
                Purchase
            </button>
        </div>

        <!-- Divider -->
        <div class="border-t border-[#3a3a50]" />

        <!-- Features section -->
        <div class="px-8 py-8">
            <PricingFeatureList :features="plan.features" />
        </div>
    </div>
</template>
