
<script setup>
    import {ref} from 'vue'

    const isOpen = ref(false)
</script>


<template>
    <div class="w-full z-10 mb-10 lg:flex items-center justify-center hidden">
        <nav class="flex w-[80%] items-center justify-between px-20 bg-white/10 backdrop-blur-lg py-5 rounded-full border-2 border-gray-200/20">
            <p class="title flex w-full items-center justify-start text-white text-2xl font-bold">Rick Dev</p>
            <div class="w-full">
                <ul class="flex items-center justify-end gap-4">
                    <a href=""><li class="text-white font-semibold text-md relative list">Home</li></a>
                    <a href=""><li class="text-white font-semibold text-md relative list">About</li></a>
                    <a href=""><li class="text-white font-semibold text-md relative list">Project</li></a>
                    <a href=""><li class="text-white font-semibold text-md relative list">Contact Me</li></a>
                </ul>
            </div>
        </nav>
    </div>
    <div class="w-full z-10 mb-10 lg:flex items-center justify-center lg:hidden">
        <nav class="relative flex w-full items-center justify-between px-10 py-5 ">
            <div class="flex items-center justify-center w-20 h-10 bg-white/10 backdrop-blur-lg rounded-full border-2 border-gray-200/20">
                <p class="text-white text-lg font-semibold">RDev</p>
            </div>
            <div class="absolute top-5 right-10 flex flex-col items-start justify-center w-auto h-auto px-3 py-3 bg-white/10 backdrop-blur-lg rounded-lg border-2 border-gray-200/20">
                <div class="flex w-full items-center justify-end gap-10">
                    <div class="w-full" v-if="isOpen"/>
                    <div class="flex flex-col items-center justify-center w-full h-full gap-1" @click="isOpen = ! isOpen">
                        <div class="w-[20px] h-[2px] bg-white rounded-full transition-all duration-500" :class="isOpen ? 'rotate-45 translate-y-1' : ''"></div>
                        <div class="w-[20px] h-[2px] bg-white rounded-full transition-all duration-500" :class="isOpen ? 'opacity-0' : ''"></div>
                        <div class="w-[20px] h-[2px] bg-white rounded-full transition-all duration-500" :class="isOpen ? '-rotate-45 -translate-y-2' : ''"></div>
                    </div>
                </div>
                <div class="w-full transition-all duration-1000" :class="isOpen ? 'block' : 'hidden'">
                <ul class="flex flex-col items-center justify-end gap-4 px-10 py-5">
                    <a href=""><li class="text-white font-semibold text-md relative list">Home</li></a>
                    <a href=""><li class="text-white font-semibold text-md relative list">About</li></a>
                    <a href=""><li class="text-white font-semibold text-md relative list">Project</li></a>
                    <a href=""><li class="text-white font-semibold text-md relative list">Contact Me</li></a>
                </ul>
                </div>
            </div>
        </nav>
    </div>
</template>

<style scope>
.list::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 2px;
    left: 0;
    bottom: -5px;
    background: linear-gradient(to right, #27FF64, #7cff67);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
}

.list:hover::after {
    transform: scaleX(1);
}
</style>
