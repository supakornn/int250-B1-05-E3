<script setup>
defineProps({
    features: {
        type: Array,
        required: true,
    },
});
</script>

<template>
    <ul class="flex flex-col gap-3">
        <li
            v-for="feature in features"
            :key="feature"
            class="flex items-center gap-3 text-gray-300 text-sm"
        >
            <svg
                class="w-4 h-4 text-purple-400 shrink-0"
                fill="none"
                stroke="currentColor"
                stroke-width="2.5"
                viewBox="0 0 24 24"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M5 13l4 4L19 7"
                />
            </svg>
            {{ feature }}
        </li>
    </ul>
</template>
