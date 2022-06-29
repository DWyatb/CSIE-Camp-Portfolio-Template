<script setup>
import { ref } from "vue";
import MdiGithub from "~icons/mdi/github";
import MdiInstagram from "~icons/mdi/instagram";
import MdiYouTube from "~icons/mdi/youtube";
import MdiFacebook from "~icons/mdi/facebook";
import Typing from "@components/Typing.vue";

const step = ref(0);
</script>
<template>
    <div class="w-full overflow-y-auto px-8 pt-16 sm:px-12 sm:pt-20 lg:px-16 lg:pt-24">
        <Typing
            v-if="step >= 0"
            @done="step++"
            text="HAHA Portfolio"
            class="mb-2 block text-2xl sm:text-3xl lg:text-4xl"
        />
        <Typing v-if="step >= 1" @done="step++" text="Hello hello!" :speed="60" />
        <a
            v-if="step >= 2"
            class="mt-8 flex items-center text-lg text-gray-500 transition-all hover:text-orange-700"
            href="https://www.youtube.com/watch?v=Eeav8s1v-_Q"
            target="_blank"
        >
            <MdiYouTube class="mr-1 inline-block text-red-500" />
            <Typing v-if="step >= 2" @done="step++" text="YouTube" :speed="60" />
        </a>
        <a
            v-if="step >= 3"
            @done="step++"
            class="mt-4 flex items-center text-lg text-gray-500 transition-all hover:text-blue-500"
            href="https://zh-tw.facebook.com/proware.tw/"
            target="_blank"
        >
            <MdiFacebook class="mr-1 inline-block text-blue-500" />
            <Typing v-if="step >= 3" @done="step++" text="FaceBook" :speed="60" />
        </a>
    </div>
</template>
