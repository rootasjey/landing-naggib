<template>
  <div class="bg-[#FAFAF9]">
    <div class="absolute -mt-16 w-full h-16 bg-black">
      <!-- <div class="bg-gradient-to-b from-black to-transparent absolute h-16 w-full z-1"></div> -->
      <NuxtImg src="/images/bg-people-1.jpg" alt="Who I Help" :modifiers="{ blur: 25 }" class="w-full h-full absolute object-cover brightness-70" />
    </div>
    <!-- Hero Section -->
    <div class="py-24 bg-gray-50 dark:bg-[#FAFAFA]">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <span>•</span>
          <h3 class="uppercase font-700">Clients</h3>
          <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">
            Organizations I've Worked With
          </h2>
          <p class="mt-4 max-w-2xl mx-auto text-gray-600 dark:text-gray-400">
            Over the years, I've had the privilege of working with leaders from various prestigious organizations.
            Here are some of the brands that have trusted me with their leadership development.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12 max-w-6xl mx-auto">
          <div v-for="(brand, index) in brands" :key="index" 
            class="bg-white dark:bg-[#11111B] rounded-lg p-8 shadow-sm hover:shadow-md transition-all duration-300
            border border-gray-200 dark:border-gray-700 flex flex-col items-center">
            <div class="w-48 h-32 flex items-center justify-center mb-6">
              <NuxtImg 
                :src="`/images/brands/${brand.logo}`" 
                :alt="`${brand.name} logo`"
                class="max-h-full max-w-full object-contain"
              />
            </div>
            <h3 class="text-xl font-semibold mb-2">{{ brand.name }}</h3>
            <p class="text-gray-600 dark:text-gray-400 text-center">{{ brand.description }}</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Testimonials Section -->
    <div class="py-16 bg-[#FFF] dark:bg-[#11111B]">
      <div class="flex flex-col justify-center items-center w-full">
        <span>•</span>
        <h3 class="uppercase font-700">Client Feedback</h3>
        <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">What they say about our work</h2>
      </div>

      <div class="mt-12 max-w-6xl mx-auto px-4">
        <div class="grid grid-cols-1 gap-8">
          <div v-for="(testimonial, index) in testimonials" :key="index" 
            class="p-8 md:p-12 
            border border-gray-200 dark:border-gray-700 rounded-2
            hover:shadow-md transition-all duration-300"
          >
            <div class="flex flex-col md:flex-row gap-8">
              <div class="md:w-1/4 flex items-start">
                <div class="w-12 h-12 bg-primary-100 dark:bg-#F5C45E rounded-full flex items-center justify-center text-primary-500">
                  <NuxtImg :src="testimonial.avatar" class="w-10 h-10 object-cover rounded-full" />
                </div>
                <div class="ml-4">
                  <h4 class="font-700">{{ testimonial.author }}</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-400">{{ testimonial.role }}</p>
                  <p class="text-xs text-gray-500 dark:text-gray-500">{{ testimonial.location }}</p>
                </div>
              </div>
              <p class="md:w-3/4 text-size-6 font-body text-gray-700 dark:text-gray-300">
                "{{ testimonial.review }}"
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CTA Section -->
    <div class="py-16 bg-[#FAFAF9] dark:bg-[#11111B] curved">
      <div class="max-w-4xl mx-auto text-center px-4">
        <h2 class="text-size-10 font-200 mb-6">Ready to transform your leadership?</h2>
        <p class="text-lg text-gray-600 dark:text-gray-400 mb-8">
          Let's discuss how I can help you and your organization achieve your leadership goals.
        </p>
        <UButton
          label="Get in touch"
          btn="primary"
          rounded="full"
          size="lg"
          to="/contact"
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const brands = [
  {
    name: 'Ikea', 
    logo: 'ikea.svg',
    description: 'Worked with senior leadership team on organizational transformation and team building.',
    url: 'https://www.ikea.com/',
  },
  {
    name: 'Porsche', 
    logo: 'porsche.svg',
    description: 'Provided executive coaching for regional directors and facilitated leadership workshops.',
    url: 'https://www.porsche.com/',
  },
  {
    name: 'GE Healthcare', 
    logo: 'ge-healthcare.svg',
    description: 'Delivered keynote speeches and leadership training for management teams across Europe.',
    url: 'https://www.gehealthcare.com/',
  },
  {
    name: 'Zalando', 
    logo: 'zalando.svg',
    description: 'Coached C-suite executives on strategic leadership and organizational development.',
    url: 'https://www.zalando.com/',
  },
  {
    name: 'BBC Radio Guernsey', 
    logo: 'bbc.svg',
    description: 'Consulted on leadership communication strategies and team performance improvement.',
    url: 'https://www.bbc.co.uk/',
  },
  {
    name: "FSD Africa",
    description: "Helped to develop specific leadership development programs for the organization's top talent.",
    logo: "fsd-africa.webp",
    url: "https://www.sharpist.com/",
  },
  {
    name: "African Leadership Group",
    description: "Brought in a clearer vision and direction for the organization's leadership development efforts.",
    logo: "african-leadership-group.webp",
    url: "https://algroup.org/",
  },
  {
    name: "Watoto",
    description: "Simplified the organization and management for more efficient operations.",
    logo: "watoto.webp",
    url: "https://www.watoto.com/",
  },
  {
    name: "LVMH",
    description: "Brought a closer alignment between leadership and employees, leading to increased productivity and engagement.",
    logo: "lvmh.png",
    url: "https://lvmh.com/",
  },
  {
    name: "RWE",
    description: "Closed the gap between the vision and the reality of the organization.",
    logo: "rwe.svg",
    url: "https://lvmh.com/",
  },
  {
    name: "home to go",
    description: "Helped managers to be more relaxed and more in control of their emotions.",
    logo: "home-to-go.webp",
    url: "https://www.hometogo.fr/",
  },
  {
    name: "Sharpist",
    description: "Developed together with the CEO a new vision for the organization.",
    logo: "sharpist.webp",
    url: "https://www.sharpist.com/",
  },
];

const testimonials = [
  {
    author: "Alina D.",
    avatar: "https://randomuser.me/api/portraits/women/1.jpg",
    role: "CEO, Tech Innovations",
    rating: 5,
    location: "Romania",
    review: "Naggib, I want you to know that what you said the other day helped me a lot! I felt empowered and I wanna say THANK YOU for being there for me! You do have this amazing gift to empower people more than anyone I know."
  },
  {
    author: "Marcus T.",
    avatar: "https://randomuser.me/api/portraits/men/2.jpg",
    role: "Regional Director, Porsche",
    rating: 5,
    location: "Germany",
    review: "Working with Naggib transformed our leadership approach. His insights and coaching techniques helped our management team navigate complex challenges during our organizational restructuring. The results have been remarkable."
  },
  {
    author: "Sarah J.",
    avatar: "https://randomuser.me/api/portraits/women/3.jpg",
    role: "Head of HR, Ikea",
    rating: 5,
    location: "Sweden",
    review: "Naggib's workshops on purpose-driven leadership created a significant shift in how our managers approach their teams. His ability to connect with people at all levels of our organization made the training incredibly effective."
  }
];

// Set page metadata
useHead({
  title: 'Clients | Naggib Chami',
  meta: [
    { name: 'description', content: 'Organizations and brands that have worked with Naggib Chami for leadership coaching and development.' }
  ]
})
</script>

<style scoped>
.curved {
  --size: 30px;
  --R: calc(var(--size)*1.28);
  --position: bottom;

  -webkit-mask:
    radial-gradient(var(--R) at left 50% var(--position) calc(1.8*var(--size)),#000 99%,#0000 101%) 
      left calc(50% - 2*var(--size)) var(--position) 0/calc(4*var(--size)) 100%,
    radial-gradient(var(--R) at left 50% var(--position) calc(-.8*var(--size)),#0000 99%,#000 101%) 
      left 50% var(--position) var(--size)/calc(4*var(--size)) 100% repeat-x;
      
  mask:
    radial-gradient(var(--R) at left 50% var(--position) calc(1.8*var(--size)),#000 99%,#0000 101%) 
      left calc(50% - 2*var(--size)) var(--position) 0/calc(4*var(--size)) 100%,
    radial-gradient(var(--R) at left 50% var(--position) calc(-.8*var(--size)),#0000 99%,#000 101%) 
      left 50% var(--position) var(--size)/calc(4*var(--size)) 100% repeat-x;
      
  background: #fff;
  height: calc(var(--size) + 350px);
}
</style>
