<template>
    <div class="w-full z-10 mb-10 flex items-center justify-center">
        <nav class="flex w-[80%] items-center justify-between px-20 bg-white/10 backdrop-blur-lg py-5 rounded-full border-2 border-gray-200/20">
            <p class="title flex w-full items-center justify-start text-white text-2xl font-bold">Rick Dev</p>
            <div class="w-full">
                <ul class="flex items-center justify-end gap-4">
                    <a href=""><li class="text-white fotn-semibold text-md relative list">Home</li></a>
                    <a href=""><li class="text-white fotn-semibold text-md relative list">About</li></a>
                    <a href=""><li class="text-white fotn-semibold text-md relative list">Project</li></a>
                    <a href=""><li class="text-white fotn-semibold text-md relative list">Contact Me</li></a>
                </ul>
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
