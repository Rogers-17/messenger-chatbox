<script setup>

</script>
<template>
    <section id="home" class="relative min-h-screen flex items-center justify-center px-4 py-20 overflow-hidden">
    <div class="absolute inset-0 overflow-hidden z-10 px-4 py-20 ">
      <div class="absolute -top-40 -right-40 w-80 h-80 bg-blue-400 rounded-full mix-blend-multiply filter blur-xl opacity-20 animate-float"></div>
      <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-blue-500 rounded-full mix-blend-multiply filter blur-xl opacity-20 animate-float" style="animation-delay: 1s;"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-80 h-80 bg-blue-300 rounded-full mix-blend-multiply filter blur-xl opacity-20 animate-float" style="animation-delay: 2s;"></div>
    </div>
        
    <div class="max-w-[1200px] mx-auto">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 justify-center items-center z-30 container">
            <div class="">
                <h1 class="text-4xl md:text-5xl lg:text-7xl font-bold">
                    Revolutionize Customer Services With <span class="text-transparent bg-clip-text bg-linear-to-r from-[#8abeee88] to-blue-600"> Chatbot</span>
                </h1>
                <p class="text-xl text-gray-500 mt-2">
                    Say goodbye to long wait times and frustrating interactions. Our chatbot robots provide 24/7 assistance and 
                    personalized services for your customers
                </p>
                <button class="mt-2 py-4 px-7 bg-blue-500 rounded-xl text-white">
                    Get Started
                </button>
            </div>
            <div class="mt-10 md:mt-0 md:h-[648px] md:flex-1 relative">
                <img src="../../public/cog.png" alt="ArRo Chat Bot" 
                class="md:absolute h-full w-auto md:max-w-none md:-left-6 lg:left-0"  />
            </div>
        </div>
    </div>
    </section>
</template>