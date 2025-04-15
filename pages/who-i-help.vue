<template>
  <div class="min-h-screen bg-gray-50 dark:bg-[#11111B]">
    <!-- Hero Section -->
    <div class="-mt-16 bg-gray-50 dark:bg-[#11111B]">
      <div class="h-screen mx-auto flex flex-row justify-center items-center">
        <div class="absolute w-full h-full bg-black">
          <div class="bg-gradient-to-b from-black to-transparent absolute h-16 w-full z-1"></div>
          <NuxtImg src="/images/handshake-2.jpg" alt="Who I Help" :modifiers="{ blur: 25 }" class="w-full h-full absolute object-cover brightness-70" />
        </div>

        <div class="flex flex-col mt-32 color-white justify-center items-center max-w-4xl text-center z-2">
          <div class="flex gap-4">
            <NuxtLink to="#small-business-owners-section" class="relative">
              <div class="shadow-md rounded-2 w-80 hover:w-92 hover:shadow-primary/20 hover:shadow-lg transition-all duration-500 relative group">
                <NuxtImg src="/images/bg-people-1.jpg" alt="Small business owners" class="w-full h-124 object-cover brightness-90 rounded-2" />
                <h3 class="opacity-0 group-hover:opacity-100 transition-all absolute bottom-0 w-full bg-black/40 rounded-2 p-2">Small business owners</h3>
              </div>
            </NuxtLink>

            <NuxtLink to="#non-profit-organizations-section" class="relative">
              <div class="shadow-md rounded-2 w-80 hover:w-92 hover:shadow-primary/20 hover:shadow-lg transition-all duration-500 relative group">
                <NuxtImg src="/images/women-sewing-pool.webp" alt="Non-profit organizations" class="w-full h-124 object-cover brightness-90 rounded-2" />
                <h3 class="opacity-0 group-hover:opacity-100 transition-all absolute bottom-0 w-full bg-black/40 rounded-2 p-2">Non-profit organizations</h3>
              </div>
            </NuxtLink>

            <NuxtLink to="#executive-and-firs-time-leaders-section" class="relative">
              <div class="shadow-md rounded-2 w-80 hover:w-92 hover:shadow-primary/20 hover:shadow-lg transition-all duration-500 relative group">
                <NuxtImg src="/images/handshake-1.jpg" alt="Executive & first-time leaders" class="w-full h-124 object-cover brightness-90 rounded-2" />
                <h3 class="opacity-0 group-hover:opacity-100 transition-all absolute bottom-0 w-full bg-black/40 rounded-2 p-2">Executive & first-time leaders</h3>
              </div>
            </NuxtLink>
          </div>

          <h1 class="mt-6 font-body text-size-20 font-500 uppercase">
            Who I Help
          </h1>
          <p class="text-lg font-400 max-w-500px">
            You made it to the top because you have an intense self-focus on personal performance and development, closely aligned with a self-imposed discipline and goal-driven behaviour.
          </p>
        </div>
      </div>
    </div>

    <!-- Small Business Owners Section -->
    <div id="small-business-owners-section" class="py-16 bg-white dark:bg-[#0D0D17]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Building sustainable success</h3>
          <h2 class="text-size-12 font-100 text-color-gray-700 dark:text-color-gray-400">
            Small Business Owners
          </h2>
        </div>

        <div class="max-w-3xl mx-auto">
          <div class="flex flex-col gap-8 
            font-text font-300 text-size-8 prose prose-lg dark:prose-invert mx-auto"
          >
            <div class="flex flex-col gap-8 items-center">
              <p>
                Running a small business is most people's dream. 
                A dream that is associated with great freedom and financial independence. 
                Any business owner will tell you that it isn't always that straight forward. 
              </p>

              <p>
                As your coach, I will work with you to create a robust plan for moving forward. 
                I will partner with you to support and hold you accountable to make 
                that plan a reality for your business. 
              </p>

              <div class="my-12 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
                <h4 class="font-600 text-size-6 mb-4">Your benefits:</h4>
                <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                  <li>Regain control on your business</li>
                  <li>Focus on your business strategy instead of being consumed by worry in survival mode</li>
                  <li>Embark on the next phase of growth for your business</li>
                  <li>Get the support of an experienced management team</li>
                </ul>
              </div>

              <p>
                I will bring clarity to your thinking and help you to believe in yourself again. 
                I will help you not to let the mistakes and disappointments of the past control 
                and direct your future.
              </p>
            </div>

            <div class="my-12 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="font-600 text-size-6 mb-4">A better self:</h4>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Improve your leadership skills</li>
                <li>Learn to delegate and trust</li>
                <li>Let yourself time to dream</li>
                <li>Become a result-driven instead of task-oriented person</li>
                <li>Build time each day to think of your company's vision</li>
                <li>Learn how to develop and inspire your team</li>
              </ul>
            </div>

            <p>
              My approach combines practical business strategies with leadership development, helping you build both a successful company and a fulfilling entrepreneurial journey.
            </p>

            <div class="border b-dashed p-6 rounded-2 grid md:grid-cols-2 gap-4 text-size-4">
              <div class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-md">
                <h4 class="font-600 mb-3">Strategic Vision</h4>
                <p class="text-gray-700 dark:text-gray-300">
                  Clarify your business direction and develop actionable plans that align with your values and goals.
                </p>
              </div>

              <div class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-md">
                <h4 class="font-600 mb-3">Team Development</h4>
                <p class="text-gray-700 dark:text-gray-300">
                  Build and lead high-performing teams that can execute your vision even when you're not present.
                </p>
              </div>
            </div>

            <div class="my-12 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <p class="text-size-8 font-300 pl-6 space-y-2">
                <span class="i-ph-less-than-bold text-size-5 mb-1 color-primary"></span>
                <b class="color-primary">25%</b> of small businesses provide training for their employees (including owners)
              </p>
            </div>

            <div>
              <h4 class="text-center text-size-4 font-500 mb-0">They work with us</h4>
              <p class="text-center">👇</p>
            </div> 
            <div class="border p-4 rounded-lg">
              <div class="flex flex-col gap-4">
                <div v-for="(brand, index) in _smallBrands" :key="index" 
                  class="h-42 w-ful group
                  bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 
                  flex flex-row gap-1 items-center justify-between
                  shadow-none shadow-gray-200 dark:shadow-gray-800
                  border border-transparent dark:border-gray-700
                  cursor-pointer active:scale-99 transition-all duration-300
                  hover:border-primary hover:border-primary-500
                  hover:shadow-lg hover:shadow-primary-500/30
                  active:shadow-none"
                >
                  <NuxtLink :to="brand.url" target="_blank" external class="">
                    <NuxtImg :src="brand.logo" class="h-28 w-50 object-cover rounded-2 grayscale group-hover:grayscale-0" />
                  </NuxtLink>

                  <div class="p-1 flex flex-col w-2/3">
                    <h3 class="font-500 text-size-4 text-gray-700">{{ brand.name }}</h3>
                    <p class="mt-1 mr-1 text-size-3.5 text-gray-600 dark:text-gray-400">
                      {{ brand.description }}
                    </p>
                    <NuxtLink :to="brand.url" target="_blank" external class="mt-2 text-size-3 font-500 hover:underline">
                      View Website
                      <span class="i-ph-arrow-up-right"></span>
                    </NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Non-Profit Organizations Section -->
    <div id="non-profit-organizations-section"  class="py-16 bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Maximizing mission impact</h3>
          <h2 class="text-size-12 font-100 dark:text-color-gray-400">
            Non-Profit Organizations
          </h2>
        </div>

        <div class="max-w-3xl mx-auto">
          <div class="flex flex-col gap-8 
            font-text font-300 text-size-8 prose prose-lg dark:prose-invert mx-auto"
          >
            <NuxtImg 
              src="/images/women-sewing-pool.webp" alt="Non-Profit" 
              width="300" 
              class="rounded-lg mx-auto" 
            />

            <div class="flex flex-col gap-8 items-center">
              <p>
                Non-profit leaders balance mission fulfillment with operational realities, often with limited resources and high stakeholder expectations. I help you navigate these unique challenges with purpose-driven leadership approaches.
              </p>
              <p>
                My experience working with non-profit organizations has given me insight into the specific leadership skills needed to drive meaningful change while maintaining organizational sustainability.
              </p>
            </div>

            <div class="my-12 border b-dashed bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="font-600 text-size-6 mb-4">How I help non-profit organizations:</h4>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Align leadership teams around mission and strategic priorities</li>
                <li>Develop board and staff relationships that leverage everyone's strengths</li>
                <li>Create sustainable funding and operational models</li>
                <li>Build resilience in the face of changing funding landscapes</li>
                <li>Implement effective volunteer management strategies</li>
                <li>Measure and communicate impact to stakeholders</li>
              </ul>
            </div>

            <p>
              My programs help non-profit leaders create greater impact while building sustainable organizations that can fulfill their missions for years to come.
            </p>

            <div class="my-12 dark:bg-[#1A1A2E] p-6 border b-dashed flex flex-col items-center rounded-lg">
              <h4 class="font-600 text-size-6">Mission-driven leadership development</h4>
              <div class="flex gap-14 text-size-6 font-200 mt-12">
                <div class="flex flex-col items-center gap-2">
                  <span class="i-ph-heart"></span>
                  <span>Purpose</span>
                </div>
                <div class="flex flex-col items-center gap-2">
                  <span class="i-ph-users-three"></span>
                  <span>People</span>
                </div>
                <div class="flex flex-col items-center gap-2">
                  <span class="i-ph-chart-line-up"></span>
                  <span>Performance</span>
                </div>
              </div>
            </div>


            <div class="my-12 bg-white dark:bg-[#1A1A2E] p-6 rounded-lg">
              <p class="text-size-8 font-300 pl-6 space-y-2">
                <b class="color-primary">96%</b> of non-profit organizations are satisfied with their leadership development programs
              </p>
            </div>

            <div>
              <h4 class="text-center text-size-4 font-500 mb-0">They work with us</h4>
              <p class="text-center">👇</p>
            </div>

            <div class="border p-4 rounded-lg">
              <div class="flex flex-col gap-4">
                <div v-for="(brand, index) in _nonProfitBrands" :key="index" 
                  class="h-42 w-ful group
                  bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 
                  flex flex-row gap-1 items-center justify-between
                  shadow-none shadow-gray-200 dark:shadow-gray-800
                  border border-transparent dark:border-gray-700
                  cursor-pointer active:scale-99 transition-all duration-300
                  hover:border-primary hover:border-primary-500
                  hover:shadow-lg hover:shadow-primary-500/30
                  active:shadow-none"
                >
                  <NuxtLink :to="brand.url" target="_blank" external class="">
                    <NuxtImg :src="brand.logo" class="h-28 w-50 object-cover rounded-2 grayscale group-hover:grayscale-0" />
                  </NuxtLink>

                  <div class="p-1 flex flex-col w-2/3">
                    <h3 class="font-500 text-size-4 text-gray-700">{{ brand.name }}</h3>
                    <p class="mt-1 mr-1 text-size-3.5 text-gray-600 dark:text-gray-400">
                      {{ brand.description }}
                    </p>
                    <NuxtLink :to="brand.url" target="_blank" external class="mt-2 text-size-3 font-500 hover:underline">
                      View Website
                      <span class="i-ph-arrow-up-right"></span>
                    </NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Executives & First-Time Leaders Section -->
    <div id="executive-and-firs-time-leaders-section"  class="py-16 bg-white dark:bg-[#0D0D17]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Leadership at every level</h3>
          <h2 class="text-size-12 font-100 dark:text-color-gray-400">
            Executives & First-Time Leaders
          </h2>
        </div>

        <div class="max-w-3xl mx-auto">
          <div class="flex flex-col gap-8 
            font-text font-300 text-size-8 prose prose-lg dark:prose-invert mx-auto"
          >
            <NuxtImg 
              src="/images/anne-marie-chidzero-portrait.webp" alt="Non-Profit" 
              width="300" 
              class="rounded-lg mx-auto" 
            />
            <p>
              You made it to the top because you have an intense self-focus on personal performance and development, 
              closely aligned with a self-imposed discipline and goal-driven behaviour. 
            </p>
            
            <p>
              But you know that your success has come at a cost. 
              Along the way, your relationships, time, balance and maybe even your health, have suffered.
            </p>

            <div class="my-12 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="font-600 text-size-6 mb-4">You feel:</h4>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Passionate about your work, competitive and driven to get results</li>
                <li>Stress, anxiety, depression and your life balance as unhealthy</li>
                <li>Acquainted with loneliness and isolation and prone to self-sabotaging behaviour</li>
              </ul>
            </div>

            <p>
              Whether you're stepping into leadership for the first time or navigating the complexities of executive leadership, I provide tailored support to help you excel in your role and create lasting impact.
            </p>

            <div class="bg-[#FAFAF9] dark:bg-[#1A1A2E] py-12 rounded-2 mt-12 w-full flex flex-wrap justify-center gap-2 items-center">
              <div class="w-68 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 flex flex-col
                border border-dashed border-gray-300 dark:border-gray-700
                cursor-pointer hover:scale-101 active:scale-99 transition-all duration-300
                hover:border-solid hover:border-primary-500
                flex justify-center items-center"
              >
                <span class="i-ph-crown text-size-4 font-700 bg-primary-500 text-white rounded-full w-6 h-6 flex justify-center items-center" />

                <div class="text-center flex flex-col">
                  <h3 class="font-800">Seasoned Executives</h3>
                  <p class="mt-6 text-sm text-gray-600 dark:text-gray-400">
                    Refine your leadership approach, navigate complex organizational challenges, and create lasting legacy through strategic vision and people development.
                  </p>
                </div>
              </div>

              <div class="w-68 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 flex flex-col
                border border-dashed border-gray-300 dark:border-gray-700
                cursor-pointer hover:scale-101 active:scale-99 transition-all duration-300
                hover:border-solid hover:border-primary-500
                flex justify-center items-center"
              >
                <span class="i-ph-shooting-star text-size-4 font-700 bg-primary-500 text-white rounded-full w-6 h-6 flex justify-center items-center" />

                <div class="text-center flex flex-col">
                  <h3 class="font-800">First-Time Leaders</h3>
                  <p class="mt-6 text-sm text-gray-600 dark:text-gray-400">
                    Build confidence in your leadership abilities, develop essential management skills, and create a leadership style that's authentic to you and effective with your team.
                  </p>
                </div>
              </div>
            </div>

            <p>
              We understand that it is of fundamental importance, when coaching and mentoring high achievers, 
              to establish a coaching relationship built on trust and mutual respect. 
              We also understand that success is not a destination, it is a process. 
              As part of this process, we make sure that your goals are clear and are the central focus of our coaching.
              We will help you identify specific actions that will deliver short-term as well as your long-term goals.
            </p>

            <p>
              Together, we will develop and implement strategies that will give you balance and peace of mind 
              to cope with the demands of being a high achiever at the top of your game.
            </p>

            <div class="my-2 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <div class="flex gap-2">
                <i class="i-ph-crown-simple-duotone text-size-6 mt-1"></i>
                <h4 class="font-600 text-size-6 mb-4">
                  Executives benefits:
                </h4>
              </div>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Strategic thinking and decision-making frameworks</li>
                <li>Executive presence and influential communication</li>
                <li>Leading organizational change and transformation</li>
                <li>Building high-performing leadership teams</li>
                <li>Succession planning and legacy development</li>
              </ul>
            </div>

            <div class="my-2 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <div class="flex gap-2">
                <i class="i-ph-medal-military-duotone text-size-6 mt-1"></i>
                <h4 class="font-600 text-size-6 mb-4">
                  First-time leaders benefits:
                </h4>
              </div>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Essential management skills and frameworks</li>
                <li>Confidence building and imposter syndrome management</li>
                <li>Effective delegation and team development</li>
                <li>Difficult conversations and conflict resolution</li>
                <li>Time management and priority setting</li>
              </ul>
            </div>

            <p>
              My coaching and training programs are tailored to your specific leadership context, helping you navigate challenges with confidence and create meaningful impact in your organization.
            </p>

            <div>
              <h4 class="text-center text-size-4 font-500 mt-12">They work with us</h4>
              <p class="text-center">👇</p>
            </div>

            <div class="border p-4 rounded-lg">
              <div class="flex flex-col gap-4">
                <div v-for="(brand, index) in _leaderBrands" :key="index" 
                  class="h-42 w-ful group
                  bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 
                  flex flex-row gap-1 items-center justify-between
                  shadow-none shadow-gray-200 dark:shadow-gray-800
                  border border-transparent dark:border-gray-700
                  cursor-pointer active:scale-99 transition-all duration-300
                  hover:border-primary hover:border-primary-500
                  hover:shadow-lg hover:shadow-primary-500/30
                  active:shadow-none"
                >
                  <NuxtLink :to="brand.url" target="_blank" external class="">
                    <NuxtImg :src="brand.logo" class="h-28 w-50 object-contain rounded-2 grayscale group-hover:grayscale-0" />
                  </NuxtLink>

                  <div class="p-1 flex flex-col w-2/3">
                    <h3 class="font-500 text-size-4 text-gray-700">{{ brand.name }}</h3>
                    <p class="mt-1 mr-1 text-size-3.5 text-gray-600 dark:text-gray-400">
                      {{ brand.description }}
                    </p>
                    <NuxtLink :to="brand.url" target="_blank" external class="mt-2 text-size-3 font-500 hover:underline">
                      View Website
                      <span class="i-ph-arrow-up-right"></span>
                    </NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Client Success Stories Section -->
    <div class="py-16 bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Real Results</h3>
          <h2 class="text-size-12 font-100 text-color-gray-700 dark:text-color-gray-400">
            Client Success Stories
          </h2>
        </div>
        
        <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-8">
          <div v-for="(testimonial, index) in _testimonials" :key="index" 
            class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-sm
             flex flex-col justify-between">
            <p class="italic text-gray-700 dark:text-gray-300 mb-4">
              "{{ testimonial.review }}"
            </p>
            <p class="font-500">{{ testimonial.author }}, {{ testimonial.role }}</p>
          </div>
        </div>
      </div>
    </div>

    <!-- CTA Section -->
    <div class="curved py-16 bg-transparent text-center">
      <div class="container mx-auto px-4">
        <h2 class="color-white text-size-4xl font-500 mb-2">
          Ready to transform your leadership?
        </h2>
        <p class="text-lg text-gray-300 max-w-2xl mx-auto mb-8">
          Let's discuss how I can help you achieve your leadership goals and create lasting impact.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <UButton label="Contact me" btn="outline" color="white" class="hover:bg-primary" href="/contact" />
          <UButton label="Schedule a consultation" btn="solid" href="/contact" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

const _smallBrands = [
  { 
    name: "Sharpist",
    description: "At Sharpist, we empower your employees to reach their full potential and drive organizational growth through our innovative digital coaching platform.",
    logo: "/images/brands/sharpist.webp",
    url: "https://www.sharpist.com/",
  },
  { 
    name: "home to go",
    description: "The world's largest selection of vacation rentals",
    logo: "/images/brands/home-to-go.webp",
    url: "https://www.hometogo.fr/",
  },
];

const _nonProfitBrands = [
  { 
    name: "FSD Africa",
    description: "FSD Africa is incorporated as a non-profit company limited by guarantee in Kenya. It is funded by UK aid from the UK government.",
    logo: "/images/brands/fsd-africa.webp",
    url: "https://www.sharpist.com/" 
  },
  { 
    name: "African Leadership Group",
    description: "We are transforming Africa by developing 3 million ethical, entrepreneurial leaders at a speed and scale never before seen.",
    logo: "/images/brands/african-leadership-group.webp",
    url: "https://algroup.org/",
  },
  { 
    name: "Watoto",
    description: "Watoto brings hope and healing to vulnerable women and children in Uganda and South Sudan. We aim at the pain in our communities and invite you to join us.",
    logo: "/images/brands/watoto.webp",
    url: "https://www.watoto.com/",
  },
];

const _leaderBrands = [
  { 
    name: "BBC",
    description: "Listen live to BBC Radio Guernsey on BBC Sounds.",
    logo: "/images/brands/bbc.svg",
    url: "https://www.bbc.co.uk/sounds/play/live/bbc_radio_guernsey"
  },
  { 
    name: "Ikea",
    description: "Furniture, home accessories, design ideas and inspiration for big dreams and small budgets. A better everyday life begins at home!",
    logo: "/images/brands/ikea.svg",
    url: "https://ikea.com/",
  },
  { 
    name: "Zalando",
    description: "International online retailer based in Berlin which is active across Europe and specializes in shoes, fashion and beauty products.",
    logo: "/images/brands/zalando.svg",
    url: "https://www.zalando.com/",
  },
];

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
]

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
      
  background: #3A59D1;
  height: calc(var(--size) + 350px);
}
</style>
