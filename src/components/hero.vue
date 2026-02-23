<script setup lang="ts">
    import RotatingText from './RotatingText.vue';
</script>

<template>
    <div class="relative w-full h-[80vh] flex flex-col items-center justify-center px-20">
    <h1 class="text-[300px] font-extrabold text-white/20 mt-20">HOLAAAA</h1>
    <div class="relative grid grid-cols-3 gap-10 text-white z-10 w-full">
        <div class="flex flex-col items-start justify-center pr-10 gap-2">
            <h1 class="text-4xl font-extrabold text-white">ERICK PRAWIRA</h1>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Hic, corporis dolore veniam sequi, in error nihil molestiae fugit rem reiciendis ex ipsum? Quas quod laudantium tempore quo nesciunt repellat amet?</p>
        </div>
        <div class="flex items-center justify-center w-full">
            <button class="button relative bg-white/10 backdrop-blur-lg text-white px-12 py-4 rounded-full border-2 border-white/20 overflow-hidden hover:-translate-y-2 transition-all duration-500">Load More</button>
        </div>
        <div class="flex flex-col items-end justify-center gap-6">
            <div class="flex items-center justify-center gap-4">
                <h1 class="text-3xl font-bold">I'am a</h1>
                <RotatingText
                 :texts="['Front End Developer', 'Fullstack Developer', 'BackEnd Developer', 'UIUX Designer']"
                 mainClassName="px-2 sm:px-2 md:px-3 bg-[#7cff67] text-black text-2xl font-bold overflow-hidden py-0.5 sm:py-1 md:py-2 justify-center rounded-lg"
                 :staggerFrom="'last'"
                 :initial="{ y: '100%' }"
                 :animate="{ y: 0 }"
                 :exit="{ y: '-120%' }"
                 :staggerDuration="0.025"
                 splitLevelClassName="overflow-hidden pb-0.5 sm:pb-1 md:pb-1"
                 :transition="{ type: 'spring', damping: 30, stiffness: 400 }"
                 :rotationInterval="2000"
                 />
            </div>
            <div class="flex items-center justify-between gap-5">
                <div class="logo overflow-hidden text-white bg-white/10 backdrop-blur-lg px-4 py-4 rounded-full border-2 border-white/20">
                    <img src="../assets/image/github.png" alt="" class="w-8 h-8">
                </div>
                <div class="logo overflow-hidden text-white bg-white/10 backdrop-blur-lg px-4 py-4 rounded-full border-2 border-white/20">
                    <img src="../assets/image/linkedin.png" alt="" class="w-8 h-8">
                </div>
                <div class="logo overflow-hidden text-white bg-white/10 backdrop-blur-lg px-4 py-4 rounded-full border-2 border-white/20">
                    <img src="../assets/image/instagram.png" alt="" class="w-8 h-8">
                </div>
            </div>
        </div>
    </div>
        <!-- <button class="bg-white/10 backdrop-blur-lg text-white px-12 py-4 rounded-full border-2 border-white/20">More</button> -->
    <img src="../assets/image/me.png" alt="" class="absolute top-0 right-1/2 translate-x-1/2 w-[700px] h-auto">
    </div>
</template>

<style scope>
    .button::before {
        content: '';
        position: absolute;
        width: 100%;
        height: 50%;
        left: 0;
        bottom: -20px;
        background: linear-gradient(to right,#7cff67, #27FF64, #23ee04);
        transform: scale(0);
        transform-origin: bottom;
        transition: transform 0.3s ease;
        z-index: -1;
        filter: blur(20px);
    }

    .button:hover::before{
        transform: scale(1);
    }

    .logo::before {
        content: '';
        position: absolute;
        width: 100%;
        height: 50%;
        left: 0;
        bottom: -2px;
        background: linear-gradient(to right,#7cff67, #27FF64, #23ee04);
        transform: scale(0);
        transform-origin: bottom;
        transition: transform 0.3s ease;
        z-index: -1;
        filter: blur(20px);
    }

    .logo:hover::before{
        transform: scale(1);
    }
</style>

