<template>
  <section id="faqs" class="py-16 px-6 bg-blue-50">
    <div class="max-w-2xl mx-auto">
      
      <!-- Title -->
  <div class="text-center mb-12">
        <h2 class="text-3xl font-bold text-slate-900">Frequently Asked Questions</h2>
        <p class="text-slate-600 mt-2">Here are some common questions and answers</p>
      </div>
      

      <!-- FAQ Items -->
      <div class="space-y-4">
        <div
          v-for="item in faqList" :key="item.id" class="bg-white rounded-lg border p-4"
          :class="{ 'border-blue-500': item.id === openId }"
        >
          <!-- Question -->
          <button class="w-full text-left flex justify-between items-center" @click="toggleFaq(item.id)" >
            <span class="font-semibold text-slate-900"> {{ item.question }} </span>

            <span class="text-xl text-blue-600"> {{ openId === item.id ? '-' : '+' }} </span>
          </button>

          <!-- Answer -->
          <div class="overflow-hidden transition-all duration-300" :class="openId === item.id ? 'max-h-40 mt-2' : 'max-h-0'" >
            <p class="text-slate-600"> {{ item.answer }} </p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script>
export default {
  name: "FAQs",

  // Component Data
  data() {
    return {
      // the FAQ that opens by default
      openId: 1, 

      // list of FAQs
      faqList: [
        {
          id: 1,
          question: "How does the chatbot work?",
          answer:
            "Our chatbot uses AI to understand questions and give helpful answers."
        },
        {
          id: 2,
          question: "Can I customize it?",
          answer:
            "Yes, you can change the chatbot's style, tone, and responses."
        },
        {
          id: 3,
          question: "What platforms does it support?",
          answer:
            "It works on Facebook Messenger, websites, mobile apps, and more."
        },
        {
          id: 4,
          question: "Is there a free trial?",
          answer:
            "Yes! You get a 14-day free trial with full access."
        },
        {
          id: 5,
          question: "Is my data secure?",
          answer:
            "We encrypt all data and follow major privacy laws like GDPR."
        },
        {
          id: 6,
          question: "Does it support multiple languages?",
          answer:
            "Yes! It supports over 50 languages and can auto-detect the user’s language."
        }
      ]
    };
  },

  // Component Methods
  methods: {
    toggleFaq(id) {
      // if clicked again, close; otherwise open
      this.openId = this.openId === id ? null : id;
    }
  }
};
</script>