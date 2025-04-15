<template>
  <div>
    <!-- Hero Section -->
    <div class="-mt-16 flex justify-center items-center w-full h-screen">
      <NuxtImg 
        class="w-full h-full object-cover brightness-90
        hover:scale-102 transition-transform duration-500 ease-in-out"
        src="/images/naggib-hero-2.jpeg"
      />

      <div class="invisible absolute pointer-events-none w-90% h-90% border-4 border-solid b-primary rounded-4"></div>
      <div class="invisible absolute pointer-events-none translate--1 w-90% h-90% border-4 border-solid b-primary-200 rounded-4"></div>

      <div class="absolute bottom-12 text-center flex flex-col text-gray-300">
        <h1 class="font-title text-size-6xl font-800 uppercase">
          Lead with Purpose & Passion
        </h1>
        <p class="text-lg font-400 text-gray-300">
          Your personal, professional coach.
        </p>

        <UButton 
          icon 
          btn="ghost-gray"
          rounded="full"
          label="i-ph-arrow-down-bold text-size-2xl"
          class="m-auto mt-2 text-gray-300 hover:text-primary-500 hover:scale-110 active:scale-99 transition-transform duration-300"
          @click="scrollDown()"
        />
      </div>
    </div>

    <!-- Branding Section -->
    <div class="py-24 bg-gray-50 dark:bg-[#FAFAFA]">
      <div class="container mx-auto px-4">
        <div class="text-center mb-10">
          <NuxtLink to="/clients" class="hover:underline">
            <h2 class="text-size-6 text-black font-text font-200">I support leaders from</h2>
          </NuxtLink>
        </div>
        
        <div class="flex flex-wrap justify-center items-center gap-8 md:gap-16">
          <div v-for="(brand, index) in _brands" :key="index" 
            class="w-32 h-20 flex items-center justify-center 
              grayscale hover:grayscale-0 transition-all duration-300"
            >
            <NuxtImg 
              :src="`/images/brands/${brand.logo}`" 
              :alt="`${brand.name} logo`"
              class="max-h-full max-w-full object-contain"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- Services Section -->
    <div class="my-64px">
      <div class="flex flex-col justify-center items-center w-full">
        <span>•</span>
        <h3 class="uppercase font-700">My services</h3>
        <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">
          I provide a range of services
        </h2>
      </div>

      <div class="mt-12 flex justify-center gap-12 items-center w-full">
        <div v-for="(service, index) in _services" :key="index" 
          class="h-72 w-54 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 
          flex flex-col
          border border-dashed border-gray-300 dark:border-gray-700
          cursor-pointer hover:scale-101 active:scale-99 transition-all duration-300
          hover:border-solid hover:border-primary-500"
        >
          <NuxtLink :to="service.url">
            <NuxtImg :src="service.image" class="h-32 w-full object-cover rounded-2" />

            <div class="absolute bottom-4 p-1 flex flex-col">
              <div class="flex gap-2 items-center">
                <span :class="service.icon" class="text-size-4"></span>
                <h3 class="font-800">{{ service.name }}</h3>
              </div>
              <p class="mt-1 mr-1 text-sm text-gray-600 dark:text-gray-400">
                {{ service.description }}
              </p>
            </div>
          </NuxtLink>
        </div>
      </div>
    </div>

    <!-- Backstory Section -->
    <div class="mt-100px pb-16 pt-12 bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="flex flex-col justify-center items-center w-full">
        <span>•</span>
        <h3 class="uppercase font-700">Backstory</h3>
        <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">
          My purpose
        </h2>
      </div>
      
      <div class="w-full p-8 md:p-0 md:w-2/3 xl:w-1/2 mx-auto mt-12">
        <NuxtImg src="/images/naggib-pp.jpeg" class="w-24 h-24 object-cover rounded-full mx-auto" />
        <p class="mt-4 text-size-10 font-200 font-text text-gray-600 dark:text-gray-400">
          My passion is to add value to you, to help you discover your purpose and realise your true potential. 
          I work with individuals, executives, corporations and organisations to enhance their leadership capabilities, 
          increase their influence, and improve their teams and ultimately, their productivity, 
          without compromising their values.
        </p>

        <div class="mt-8 flex flex-col justify-center items-center">
          <UButton
            label="Let's talk"
            btn="outline"
            rounded="full"
          />
        </div>
      </div>
    </div>

    <!-- Process Section -->
    <div class="my-100px w-4xl mx-auto">
      <div class="flex flex-col justify-center items-center w-full">
        <span>•</span>
        <h3 class="uppercase font-700">The process</h3>
        <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">
          Six compelling reasons to work together
        </h2>
      </div>

      <div class="mt-12 w-full flex flex-wrap justify-center gap-12 items-center">
        <div v-for="(service, index) in _processes" :key="index" 
          class="h-78 w-58 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 flex flex-col
          border border-dashed border-gray-300 dark:border-gray-700
          cursor-pointer hover:scale-100 active:scale-99 transition-all duration-300
          hover:border-solid hover:border-primary-500"
        >
          <div class="text-size-4 font-700 bg-primary-500 text-white rounded-full w-6 h-6 flex justify-center items-center">
            {{ index + 1 }}
          </div>

          <div class="absolute bottom-4 p-1 flex flex-col">
            <h3 class="font-800">{{ service.name }}</h3>
            <p class="mt-1 mr-1 text-sm text-gray-600 dark:text-gray-400">
              {{ service.description }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Businesses Section -->
    <div class="mt-100px py-12 w-full mx-auto bg-gray-50 dark:bg-[#11111B]">
      <div class="flex flex-col justify-center items-center w-full">
        <span>•</span>
        <h3 class="uppercase font-700">Businesses</h3>
        <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">
          I'm great fit for
        </h2>
      </div>

      <div class="mt-12 w-full flex flex-wrap justify-center gap-12 items-center">
        <div v-for="(business, index) in _businesses" :key="index" 
          class="h-42 w-42 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 flex flex-col
          border border-dashed border-gray-300 dark:border-gray-700
          cursor-pointer hover:scale-101 active:scale-99 transition-all duration-300
          hover:border-solid hover:border-primary-500
          flex justify-center items-center"
        >
          <span :class="business.icon" class="text-size-4 font-700 bg-primary-500 text-white rounded-full w-6 h-6 flex justify-center items-center" />

          <div class="text-center flex flex-col">
            <h3 class="font-800">{{ business.name }}</h3>
            <p class="text-sm text-gray-600 dark:text-gray-400">
              {{ business.description }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Testimonials Section -->
    <div class="py-16 bg-[#FFF] dark:bg-[#11111B]">
      <div class="flex flex-col justify-center items-center w-full">
        <span>•</span>
        <h3 class="uppercase font-700">Testimonials</h3>
        <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">What my clients say</h2>
      </div>

      <div class="mt-12">
        <div>
          <div v-for="(testimonial, index) in _testimonials" :key="index" 
            class="p-16 flex flex-row 
            border border-gray-200 dark:border-gray-700 rounded-2
            hover:shadow-md transition-all duration-300"
          >
            <div class="w-1/3 flex items-center">
              <div class="w-12 h-12 bg-primary-100 dark:bg-#F5C45E rounded-full flex items-center justify-center text-primary-500">
                <NuxtImg :src="testimonial.avatar" class="w-10 h-10 object-cover rounded-full" />
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
        
        <div class="mt-12 flex justify-center">
          <UButton
            label="See more testimonials"
            btn="outline"
            rounded="full"
            to="/testimonials"
          />
        </div>
      </div>
    </div>

    <!-- FAQ Section -->
    <div class="py-16 bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="flex flex-col justify-center items-center w-full">
        <span>•</span>
        <h3 class="uppercase font-700">FAQ</h3>
        <h2 class="text-size-12 font-200 text-color-gray-700 dark:text-color-gray-400">Frequently Asked Questions</h2>
      </div>

      <div class="mt-12 w-full max-w-3xl mx-auto px-4">
        <UAccordion :items="_faqItems" />
      </div>
    </div>
  </div>

  <!-- Footer -->
</template>

<script lang="ts" setup>

const _brands = [
  { name: 'Ikea', logo: 'ikea.svg' },
  { name: 'Porsche', logo: 'porsche.svg' },
  { name: 'GE Healthcare', logo: 'ge-healthcare.svg' },
  { name: 'Zalando', logo: 'zalando.svg' },
  { name: 'BBC Radio Guernsey', logo: 'bbc.svg' }
];

const _services = [
  {
    icon: "i-ph:microphone-stage-duotone",
    name: "Coaching",
    description: "With over 20 years of international experience, I am an experienced executive coach.",
    image: "/images/service-coaching.webp",
    url: "/services#coaching-section",
  },
  {
    icon: "i-icon-park-outline:dumbbell",
    name: "Corporate training",
    description: "I train and coach your teams to reach your compoany goals. I help you to build highly effective team.",
    image: "/images/service-corporate-training.jpeg",
    url: "/services#corporate-training-section",
  },
  {
    icon: "i-icon-park-outline:theater",
    name: "Keynote speaking",
    description: "I transform your business and empower your employees with standard or tailored solutions.",
    image: "/images/service-keynote-speaking.jpg",
    url: "/services#keynote-speaking-section",
  },
]

const _businesses = [
  {
    icon: "i-ph:house-line-duotone",
    name: "Small businesses owners",
    description: "",
  },
  {
    icon: "i-ph:buildings-duotone",
    name: "Executives and first time leaders",
    description: "",
  },
  {
    icon: "i-ph:lighthouse-duotone",
    name: "Non-profit organisations",
    description: "",
  },
]

const _processes = [
  {
    name: "Innovative approach to problem solving",
    description: "I am able to think outside the box and come up with creative solutions to complex problems. It is always my focus to see the big picture and connect disparate ideas to help you achieve success.",
  },
  {
    name: "Wide-range expertise",
    description: "My experience extends across a variety of industries, including technology, finance, and healthcare. I’ve provided support for startups, Fortune 500 companies, and government agencies. So rest assured, whatever your position, I'll be able to support.",
  },
  {
    name: "Results driven",
    description: "When working with individuals or organisations, I know the importance of accountability when measuring results.  I combine cutting-edge strategies with personalised guidance to deliver growth and profitability. Your success is my success.",
  },
  {
    name: "Excellent communication skills",
    description: "I am a natural communicator who can explain complex concepts in simple terms. I am comfortable presenting to both technical and non-technical audiences. I will speak your language.",
  },
  {
    name: "Global perspective",
    description: "I've worked in multiple countries to support with coaching and corporate training requirements. This gives me a unique perspective on global organisational trends and cultural differences. Wherever you operate, I'll be on hand to support.",
  },
  {
    name: "Passion for social impact",
    description: "I am involved with several non-profit organisations that focus on social and environmental issues. I am passionate about using effective leadership and technology to create positive change in the world.",
  },
]

const _faqItems = [
  {
    label: "What's the difference between coaching and mentoring?",
    content: "Coaching typically focuses on improving a specific skill or achieving a particular goal, often in a professional context. Mentoring, on the other hand, tends to involve a longer-term relationship in which a more experienced person provides guidance and advice to a less experienced individual, often with the goal of career development.",
    defaultOpen: true,
  },
  {
    label: "How do you know if coaching or mentoring is right for you?",
    content: "Depending on your goals and needs, if you're looking to improve a specific skill or overcome a particular challenge, coaching may be the best option. If you're seeking more general guidance and support for your career, mentoring might be a better fit. It's important to identify your goals and be clear about what you hope to gain from the relationship.",
  },
  {
    label: "How long does coaching or mentoring typically last?",
    content: "Some coaching programs may only last a few sessions, while others may continue for several months. Mentoring relationships can last for years. It's important to discuss your expectations with your coach/mentor and determine what the best timeline is for you.",
  },
  {
    label: "How often should I meet with my coach or mentor?",
    content: "Some people may benefit from weekly meetings, while others might only need to meet once a month or even less frequently. It's important to find a schedule that works for both you and your coach/mentor.",
  },
  {
    label: "What can I expect from a coaching or mentoring session?",
    content: "Each session will be different, but generally, you can expect to discuss your goals, progress, and any challenges you’re facing. Your coach/mentor may offer advice, ask questions to help you clarify your thinking, or provide exercises to help you practice and improve your skills.",
  }
]

const _testimonials = [
  {
    author: "Alina D.",
    avatar: "https://randomuser.me/api/portraits/women/1.jpg",
    role: "CEO, Tech Innovations",
    rating: 5,
    location: "Romania",
    review: "Naggib, I want you to know that what you said the other day helped me a lot! I felt empowered and I wanna say THANK YOU for being there for me! You do have this amazing gift to empower people more than anyone I know."
  },
]

const scrollDown = () => {
  window.scrollTo({
    top: window.innerHeight,
    behavior: 'smooth'
  })
}
</script>

<style scopped>
</style>
