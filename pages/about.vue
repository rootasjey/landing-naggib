<template>
  <div class="min-h-screen bg-gray-50 dark:bg-[#11111B]">
    <!-- Hero Section -->
    <div class="-mt-16 py-24 bg-gray-50 dark:bg-[#11111B]">
      <div class="container mx-auto px-4 pt-24 flex flex-col items-center">
        <NuxtImg 
          src="/images/naggib-pp.jpeg" 
          class="w-64 h-64 object-cover rounded-full"
          alt="Naggib portrait"
        />
        <div class="max-w-4xl text-center mt-6 mb-10">
          <h1 class="font-title text-size-6xl font-800 uppercase">
            "If you don't control what you think, you can't control what you do."
          </h1>
          <p>—</p>
          <p class="text-lg font-500 text-gray-800 dark:text-gray-300 mt-4">
            Naggib Chakhane
          </p>
          <p class="text-lg font-400 text-gray-400 dark:text-gray-300">
            Leadership coach, speaker, and corporate trainer
          </p>
        </div>
      </div>
    </div>

    <!-- Certifications Section -->
    <div class="py-16 bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="container mx-auto px-4">
        <div class="border-t mb-12"></div>
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Certifications</h3>
          <h2 class="text-size-12 font-100 text-color-gray-700 dark:text-color-gray-400">
            Professional Qualifications
          </h2>
        </div>
        
        <div class="flex flex-wrap justify-center items-center gap-8 md:gap-16">
          <div v-for="(certification, index) in _certificationItems" :key="index"
          class="flex flex-col items-center"
          >
          <div class="w-20 h-20 
            rounded-full overflow-hidden cursor-pointer
            flex items-center justify-center bg-white
            border-2 border-primary border-[#3A59D1]
            shadow-md hover:shadow-lg hover:scale-105 active:scale-99
            transition-transform grayscale hover:grayscale-0 transition-all duration-300">
            <NuxtLink :to="certification.url" target="_blank">
              <NuxtImg
                :src="`${certification.image}`"
                :alt="`${certification.name} logo`"
                class="h-18 w-18 object-cover"
                />
              </NuxtLink>
          </div>
            <div class="max-w-160px mt-4 text-center">
              <span class="text-gray-500 text-size-3.5 font-600 line-height-0.2">
                {{ certification.name }}
              </span>
              <span class="block text-gray-500 text-size-2.5 font-600">
                {{ certification.description }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- About My Work Section -->
    <div class="py-16 bg-white dark:bg-[#0D0D17]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">My Approach</h3>
          <h2 class="text-size-12 font-100  dark:text-color-gray-400">
            How I Help?
          </h2>
        </div>

        <div class="max-w-3xl mx-auto">
          <div class="flex flex-col gap-12 
            font-text font-300 text-size-8 prose prose-lg dark:prose-invert mx-auto"
          >
            <p>
              Leadership can be challenging. I've walked in your shoes, and I'm here to guide you.
            </p>
            
            <p>
              Being a leader — whether you're just starting out or have years of experience — often feels like juggling too many responsibilities at once. Even if you excel at your technical role, true leadership requires something more: the ability to inspire, connect, and guide others.
            </p>
            
            <p>
              As your coach, I work with you privately to uncover your natural talents. Together, we'll find ways to use these strengths to benefit you, empower your team, and achieve the results your organization needs.
            </p>
            
            <p>
              We don't ignore your challenges — we face them head-on. We'll develop practical strategies to address areas where you're less confident, allowing you to focus on what I call <b class="color-primary">YOUR SWEET SPOT</b> — that magical intersection where your purpose, passion, and skills come together.
            </p>
            
            <p>
              Success at work means little if other parts of your life are suffering. True fulfillment comes from thriving in all areas — family, relationships, health — and making a difference in what matters to you. If you're seeking balanced success that doesn't force you to choose between career and personal life, let's connect today. Your journey to wholehearted leadership starts with a simple conversation.
            </p>
          </div>
        </div>

      </div>
    </div>

    <!-- CTA Section -->
    <div class="curved py-16 bg-transparent text-center">
      <div class="container mx-auto px-4">
        <h2 class="color-white text-size-4xl font-500 mb-2">Ready to transform your leadership?</h2>
        <p class="text-lg text-gray-300 max-w-2xl mx-auto mb-8">
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
const _certificationItems = [
  {
    name: "EMCC",
    description: "European Mentoring & Coaching Council",
    image: "/images/certifications/emcc.webp",
    url: "https://www.emccglobal.org/accreditation/eia/",
  },
  {
    name: "AoEC",
    description: "Academy of Executive Coaching",
    image: "/images/certifications/aoec.webp",
    url: "https://www.aoec.com/",
  },
  {
    name: "Maxwell",
    description: "Leadership Certified Coach",
    image: "/images/certifications/maxwell-leadership.webp",
    url: "https://www.maxwellleadership.com/build-a-business/",
  },
  {
    name: "DISC",
    description: "Human Behaviour Consultant",
    image: "/images/certifications/disc-2.webp",
    url: "https://discinsights.com/products/certified-behavioral-consultant-cbc-self-study-course-online",
  },
  {
    name: "MBA",
    description: "Finance & Corporate Strategy",
    image: "/images/certifications/surrey-mba.webp",
    url: "https://www.surrey.ac.uk/postgraduate/master-business-administration-mba",
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
