<script setup>

    const features = [
        {
            id: 1,
            title: "Smart AI Responses",
            description: "Our chatbot uses advanced AI to understand your questions and provide accurate, helpful answers in real-time.",
            icon: "brain"
        },
        {
            id: 2,
            title: "Multi-Platform Support",
            description: "Start a conversation on web and continue seamlessly on your mobile device through Facebook Messenger.",
            icon: "devices"
        },
        {
            id: 3,
            title: "Quick Actions",
            description: "Get instant access to common tasks like checking order status, tracking shipments, or finding information.",
            icon: "lightning"
        },
        {
            id: 4,
            title: "Human Handoff",
            description: "When needed, smoothly transition from bot to human agent without repeating your information.",
            icon: "users"
        },
    ]

</script>
<template>
    <section id="features" class="py-16">
        <div class="container max-w-7xl mx-auto">
            <div class="space-y-2">
                <h1 class="text-5xl font-bold text-center">
                Why Choose Chatbot?
                </h1>
                <p class="text-xl text-gray-500 text-center">
                    Designed to provide you with the best customer service experience
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 mt-8 gap-6">
                <div 
                v-for="(feature) in features"
                :key="feature.id"
                class="rounded-xl shadow-lg"
                >
                <div class="flex flex-col justify-center items-center p-6">
                    <div class="flex flex-col justify-center bg-blue-500 rounded-full p-3 mb-4">
                        <svg v-if="feature.icon === 'brain'" class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
                        </svg>
                        <svg v-else-if="feature.icon === 'devices'" class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
                        </svg>
                        <svg v-else-if="feature.icon === 'lightning'" class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                        </svg>
                        <svg v-else-if="feature.icon === 'users'" class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
                        </svg>
                    </div>
                    <div class="flex flex-col justify-center items-center text-center space-y-1">
                        <h1 class="font-bold text-2xl">
                            {{ feature.title }}
                        </h1>
                        <p class="text-gray-500">
                            {{ feature.description }}
                        </p>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
</template>