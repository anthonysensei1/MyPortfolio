<template>
    <section class="relative py-20 overflow-hidden" id="services">
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-4xl md:text-5xl font-bold text-white mb-4 text-center">
                My
                <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">
                    Services
                </span>
                <p class="text-blue-200 text-base sm:text-lg max-w-2xl mx-auto 
         px-4 sm:px-6 md:px-8 lg:px-0
         py-4 sm:py-6
         text-center" data-aos="fade-up" data-aos-delay="100">
                    I offer a combination of web development and security-focused services. My goal is to build not only
                    visually appealing applications, but also systems that are reliable, efficient, and secure.
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div v-for="(service, index) in services" :key="service.id" :data-aos="'fade-up'"
                    :data-aos-delay="(index * 100) + 200"
                    class="group relative p-8 rounded-2xl bg-linear-to-br from-gray-80/50 to-blue-900/30 backdrop-blur-sm border border-blue-500/20 hover:border-blue-400/40 transition-all duration-500 hover:transform hover:-translate-y-2">
                    <div
                        class="absolute inset-0 bg-linear-to-r from-blue-500/50 to-cyan-500/50 rounded-2xl opacity-0 duration-500 group-hover:opacity-100 transition-opacity">
                    </div>
                    <div class="relative z-10 mb-6">
                        <div
                            class="inline-flex items-center justify-center w-16 h-16 rounded-xl bg-linear-to-r from-blue-500/20 to-cyan-500/20 border-blue-400/30 group-hover:scale-110 transition-transform duration-300">
                            <component :is="service.icon" class="w-8 h-8 text-blue-400" />
                        </div>
                    </div>
                    <div class="relative z-10">
                        <h3
                            class="text-xl font-bold text-white mb-3 group:hover:text-blue-400 transition colors duration-300">
                            {{ service.name }}
                        </h3>
                        <p class="text-blue-100 leading-relaxed">
                            {{ service.description }}
                        </p>
                    </div>
                    <div
                        class="absolute bottom-6 right-6 opacity-0 group-hover:opacity-100 translate-x-4 group-hover:translate-x-0 transition-all duration-300">
                        <ArrowRightIcon class="w-6 h-6 text-cyan-400" />
                    </div>
                </div>
            </div>
            <div class="text-center mt-16" data-aos="fade-up" data-aos-delay="800">
                <div class="inline-flex flex-col sm:flex-row gap-4 items-center">
                    <button
                        class="px-8 py-4 rounded-xl border-2 border-blue-400 text-blue-400 font-semibold hover:bg-blue-400/10 transition-all duration-300 flex-items-center">
                        Get In Touch
                        <ChatBubbleLeftRightIcon class="w-5 h-5 ml-2" />
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import {
    ArrowRightIcon,
    ChartBarSquareIcon,
    ChatBubbleLeftRightIcon,
    CodeBracketIcon,
    LockClosedIcon,
    PaintBrushIcon,
    ServerStackIcon,
    ShieldCheckIcon
} from '@heroicons/vue/16/solid';

import { ref } from 'vue';


const services = ref([

    {
        id: 1,
        icon: CodeBracketIcon,
        name: 'Web Development',
        description: 'I build modern, responsive, and high-performance websites using Vue.js, Tailwind CSS, and clean code practices. From landing pages to full web applications.'
    },
    {
        id: 2,
        icon: PaintBrushIcon,
        name: "Frontend UI/UX Design",
        description: "Creating clean, user-friendly interfaces with a focus on accessibility, responsiveness, and smooth user experience across all devices.",
    },
    {
        id: 3,
        icon: ServerStackIcon,
        name: "Backend Integration",
        description: "Experience working with PHP and Laravel to connect frontend applications to databases and APIs, ensuring smooth and secure data flow.",
    },
    {
        id: 4,
        icon: ShieldCheckIcon,
        name: "Website Security Basics",
        description: "Applying security best practices such as input validation, authentication handling, and basic vulnerability prevention to protect web applications.",
    },
    {
        id: 5,
        icon: LockClosedIcon,
        name: "Ethical Hacking (Learning)",
        description: "Actively studying ethical hacking techniques including penetration testing concepts, vulnerability scanning, and security analysis.",
    },
    {
        id: 6,
        icon: ChartBarSquareIcon,
        name: "System Analysis & Planning",
        description: "Analyzing system requirements and planning scalable solutions to ensure efficient development and long-term maintainability.",
    },
]);
</script>
<style></style>