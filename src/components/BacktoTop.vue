<template>
    <button v-if="isVisible" @click="scrollToTop" class="fixed bottom-4 right-4 bg-linear-to-r from-blue-600 to-cyan-600 text-white rounded-full w-12 h-12 items-center justify-center text-xl cursor-pointer transition-opcaity duration-opacity duration-300 hover:bg-blue-600">
        <ArrowUpCircleIcon/>
    </button>
</template>
<script setup>
import { ArrowUpCircleIcon } from '@heroicons/vue/16/solid';
import { onMounted, onUnmounted, ref } from 'vue';

const isVisible = ref(false);
const handleScroll = () => {
    isVisible.value = window.scrollY > 300;
}
const scrollToTop = () => {
    window.scrollTo({top:0, behavior:'smooth'})
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll)
});

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
})
</script>