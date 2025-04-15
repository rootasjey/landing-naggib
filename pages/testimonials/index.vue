<template>
  <div class="min-h-screen">
    <!-- Hero Section -->
    <div class="-mt-16 relative bg-gray-50 dark:bg-[#11111B]">
      <div class="bg-gradient-to-b from-black to-transparent absolute h-16 w-full z-1"></div>
      <NuxtImg src="/images/bg-people-1.jpg" alt="Testimonials" class="w-full h-96 object-cover brightness-90" />
      <div class="container mx-auto py-24 text-center">
        <h1 class="font-title text-size-16 font-800 uppercase">Client Testimonials</h1>
        <p class="-mt-4 text-lg font-400 text-gray-500 dark:text-gray-300 max-w-2xl mx-auto">
          Discover what leaders and organizations have to say about their experience working with me.
        </p>
      </div>
    </div>

    <!-- Testimonials Grid -->
    <div>
      <div class="flex flex-col">
        <div v-for="(testimonial, index) in _testimonials" :key="index" 
          class="p-16 flex flex-row 
          border-b border-t border-gray-100 dark:border-gray-800
          hover:shadow-md transition-all duration-300"
        >
          <div class="w-1/3 flex items-center">
            <div class="w-12 h-12 bg-primary-100 dark:bg-#F5C45E rounded-full flex items-center justify-center text-primary-500">
              <NuxtImg :src="testimonial.avatar" alt="Avatar" class="w-10 h-10 rounded-full" />
            </div>
            <div class="ml-4">
              <h4 class="font-700">{{ testimonial.author }}</h4>
              <p class="text-sm text-gray-600 dark:text-gray-400">{{ testimonial.role }}</p>
              <p class="text-xs text-gray-500 dark:text-gray-500">{{ testimonial.location }}</p>
            </div>
          </div>
          <p class="w-4/5 text-size-6 font-body text-gray-700 dark:text-gray-300 mb-6">
            "{{ testimonial.review }}"
          </p>
        </div>
      </div>
    </div>

    <!-- CTA Section -->
    <div class="py-16 bg-gray-50 dark:bg-[#11111B] text-center">
      <div class="container mx-auto px-4">
        <h2 class="text-size-4xl font-500 mb-6">Ready to transform your leadership?</h2>
        <p class="text-lg text-gray-700 dark:text-gray-300 max-w-2xl mx-auto mb-8">
          Join these satisfied clients and discover how my coaching can help you lead with purpose and passion.
        </p>
        <UButton
          label="Get in touch"
          btn="~"
          rounded="full"
          to="/contact"
          class="mx-auto bg-[#F5C45E] hover:bg-[#F5C45E]/90 text-black font-semibold px-6"
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

const _testimonials = [
  {
    author: "Alina D.",
    avatar: "https://randomuser.me/api/portraits/women/1.jpg",
    role: "CEO, Tech Innovations",
    rating: 5,
    location: "Romania",
    review: "Naggib, I want you to know that what you said the other day helped me a lot! I felt empowered and I wanna say THANK YOU for being there for me! You do have this amazing gift to empower people more than anyone I know."
  },
  {
    author: "Anne-Marie C.",
    avatar: "https://randomuser.me/api/portraits/women/2.jpg",
    role: "Director of Operations",
    rating: 5,
    location: "South Africa",
    review: "You have amazing talent. I am testimony to your powers!! I Could not have done it without your coaching."
  },
  {
    author: "Be Boosted",
    avatar: "https://randomuser.me/api/portraits/men/1.jpg",
    role: "Founder, Sustainable Solutions",
    rating: 5,
    location: "Germany",
    review: "Thank you so much for supporting us, Naggib! \nThe participant's feedback to your keynote speech was overwhelming."
  },
  {
    author: "Cathie",
    avatar: "https://randomuser.me/api/portraits/women/4.jpg",
    role: "Non-profit Director",
    rating: 5,
    location: "London, UK",
    review: "You are an exceptional orator, who delivers his story with passion, authenticity and excellence"
  },
  {
    author: "Dominic F.",
    avatar: "https://randomuser.me/api/portraits/men/2.jpg",
    role: "Non-profit Director",
    rating: 5,
    location: "Germany",
    review: "In the name of the whole group I wanted to thank you again for enriching our conference."
  },
  {
    author: "Dr. Liliana D.",
    avatar: "https://randomuser.me/api/portraits/women/5.jpg",
    role: "Non-profit Director",
    rating: 5,
    location: "MD, USA",
    review: "If you feel confused, if you need support or you want performance, I recommend Naggib with all my heart!"
  },
  {
    author: "Nghi L.",
    avatar: "https://randomuser.me/api/portraits/women/6.jpg",
    role: "",
    rating: 5,
    location: "Germany",
    review: "I am where I am now, both professionally and mentally, thanks to you. You are an awesome coach and an amazing person."
  },
  {
    author: "Jo W",
    avatar: "https://randomuser.me/api/portraits/men/7.jpg",
    role: "",
    rating: 5,
    location: "London, UK",
    review: "It was an absolute pleasure to attend your workshop last night. They say the best trainers and coaches have a great sense of humour and are compelling storytellers - I can see why you are so successful."
  },
  {
    author: "Mariella",
    avatar: "https://randomuser.me/api/portraits/women/8.jpg",
    role: "",
    rating: 5,
    location: "USA",
    review: "Wow! Thanks so much Naggib! Life changing! I thank you again for today's talk! You found me! I promise to stay focused ! And thanks for guidance!"
  },
  {
    author: "Huw",
    avatar: "https://randomuser.me/api/portraits/men/9.jpg",
    role: "",
    rating: 5,
    location: "Brighton, UK",
    review: "Thanks again for leading us in such an effective strategy meeting last week, it really got the board more involved and armed with a new perspective, which was much needed!"
  },
]

// Set page metadata
useHead({
  title: 'Testimonials | Naggib Chakhap',
  meta: [
    { name: 'description', content: 'Read what clients say about working with Naggib Chakhap, executive coach and leadership expert.' }
  ]
})
</script>
