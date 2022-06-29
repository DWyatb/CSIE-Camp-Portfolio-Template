<script setup>
import Typing from "@components/Typing.vue";

defineProps({
    name: { type: String, default: "Project" },
    description: { type: String, default: "" },
    image: { type: String, default: "" },
    link: { type: String, default: "" },
    tags: { type: Array, default: () => [] },
});
</script>

<template>
    <div>
        <h1 class="text-2xl">Name: {{ name }}</h1>
        Description: {{ description }}<br />
        Image: {{ image }}<br />

        <a
            class="mt-8 flex items-center text-lg text-gray-500 transition-all hover:text-orange-700"
            href="https://www.google.com.tw/?hl=zh_TW"
            target="_blank"
        >
            Link: GOOGLE <br />
        </a>
        <Typing :text="tags.join(' / ')" />
    </div>
</template>
