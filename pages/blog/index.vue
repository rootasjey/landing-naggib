<template>
  <div class="min-h-screen bg-gray-50 dark:bg-[#11111B]">
    <!-- Hero Section -->
    <div class="-mt-16 bg-gray-50 dark:bg-[#11111B]">
      <div class="h-screen mx-auto flex flex-row justify-center items-center">
        <div class="absolute w-full h-full bg-black">
          <div class="bg-gradient-to-b from-black to-transparent absolute h-16 w-full z-1"></div>
          <NuxtImg src="/images/blog-hero.jpg" alt="Blog" :modifiers="{ blur: 25 }" class="w-full h-full absolute object-cover brightness-70" />
        </div>

        <div class="flex flex-col color-white justify-center items-center max-w-4xl text-center z-2">
          <h1 class="mt-6 font-body text-size-20 font-500 uppercase">
            Leadership Insights
          </h1>
          <p class="text-lg font-400 color-gray-400 max-w-500px">
            Explore articles, resources, and insights to help you grow as a leader and achieve your full potential.
          </p>
        </div>
      </div>
    </div>

    <!-- Blog Posts Section -->
    <div class="py-16 bg-white dark:bg-[#0D0D17]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Latest Articles</h3>
          <h2 class="text-size-12 font-100 dark:text-color-gray-400">
            Blog Posts
          </h2>
        </div>

        <!-- Categories Filter -->
        <div class="max-w-4xl mx-auto mb-12">
          <div class="flex flex-wrap justify-center gap-3">
            <button 
              v-for="category in _categories" 
              :key="category.id" 
              @click="selectedCategory = category.id === selectedCategory ? '' : category.id"
              class="px-4 py-2 rounded-full text-sm transition-all duration-300"
              :class="selectedCategory === category.id ? 
                'bg-primary-500 text-white' : 
                'bg-gray-100 dark:bg-[#1A1A2E] hover:bg-gray-200 dark:hover:bg-[#2A2A3E]'"
            >
              {{ category.name }}
            </button>
          </div>
        </div>

        <!-- Blog Posts Grid -->
        <div class="max-w-6xl mx-auto">
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            <div 
              v-for="post in filteredPosts" 
              :key="post.id" 
              class="bg-gray-50 dark:bg-[#1A1A2E] rounded-lg overflow-hidden shadow-sm hover:shadow-md transition-all duration-300"
            >
              <NuxtLink :to="`/blog/${post.slug}`" class="block">
                <div class="relative h-48 overflow-hidden">
                  <NuxtImg 
                    :src="post.image" 
                    :alt="post.title" 
                    class="w-full h-full object-cover transition-transform duration-500 hover:scale-105" 
                  />
                </div>
                <div class="p-6">
                  <div class="flex items-center text-gray-500 dark:text-gray-400 text-sm mb-2">
                    <span class="i-ph-calendar mr-2"></span>
                    <span>{{ formatDate(post.date) }}</span>
                    <span class="mx-2">•</span>
                    <span class="i-ph-clock mr-2"></span>
                    <span>{{ post.readTime }} min read</span>
                  </div>
                  <h3 class="text-xl font-600 mb-2 line-clamp-2">{{ post.title }}</h3>
                  <p class="text-gray-600 dark:text-gray-300 text-sm mb-4 line-clamp-3">
                    {{ post.excerpt }}
                  </p>
                </div>
              </NuxtLink>
            </div>
          </div>

          <!-- Load More Button -->
          <div class="flex justify-center mt-12">
            <UButton
              v-if="hasMorePosts"
              label="Load More Articles"
              btn="~"
              rounded="full"
              @click="loadMorePosts"
              class="mx-auto bg-[#F5C45E] hover:bg-[#F5C45E]/90 text-black font-semibold px-6"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- Newsletter Section -->
    <div class="py-16 bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="container mx-auto px-4">
        <div class="max-w-3xl mx-auto bg-white dark:bg-[#1A1A2E] rounded-lg p-8 shadow-sm">
          <div class="text-center mb-8">
            <h3 class="text-2xl font-600 mb-2">Subscribe to My Newsletter</h3>
            <p class="text-gray-600 dark:text-gray-300">
              Get the latest leadership insights and resources delivered directly to your inbox.
            </p>
          </div>
          <form @submit.prevent="subscribeToNewsletter" class="flex flex-col sm:flex-row gap-4">
            <UInput
              v-model="email"
              placeholder="Your email address"
              type="email"
              class="flex-grow"
              required
            />
            <UButton
              type="submit"
              label="Subscribe"
              btn="~"
              rounded="full"
              class="bg-[#3A59D1] hover:bg-[#3A59D1]/90 text-white font-semibold px-6"
            />
          </form>
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
          Explore my coaching, training, and speaking services to take your leadership to the next level.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <UButton
            label="Explore Services"
            btn="~"
            rounded="full"
            to="/services"
            class="mx-auto bg-[#F5C45E] hover:bg-[#F5C45E]/90 text-black font-semibold px-6"
          />
          <UButton
            label="Contact Me"
            btn="~"
            rounded="full"
            variant="outline"
            to="/contact"
            class="mx-auto color-white dark:border-white dark:text-white font-semibold px-6"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue'

// Mock data for blog posts
const _blogPosts = [
  {
    id: 1,
    title: "It Only Takes 6 Steps to Change Your Life",
    slug: "essential-leadership-skills-modern-workplace",
    excerpt: "Discover the key leadership competencies needed to thrive in today's rapidly evolving business environment.",
    content: "",
    image: "https://picsum.photos/800/500",
    date: "2023-10-15",
    readTime: 8,
    category: "leadership",
    author: "Naggib Chakhap"
  },
  {
    id: 2,
    title: "Building Resilient Teams in Times of Change",
    slug: "building-resilient-teams",
    excerpt: "Learn strategies for developing team resilience and maintaining productivity during organizational transitions.",
    content: "",
    image: "https://picsum.photos/id/1/800/500",
    date: "2023-09-28",
    readTime: 6,
    category: "team-building",
    author: "Naggib Chakhap"
  },
  {
    id: 3,
    title: "The Power of Emotional Intelligence in Leadership",
    slug: "emotional-intelligence-leadership",
    excerpt: "Explore how emotional intelligence can transform your leadership approach and improve team dynamics.",
    content: "",
    image: "https://picsum.photos/id/22/800/500",
    date: "2023-09-10",
    readTime: 7,
    category: "personal-development",
    author: "Naggib Chakhap"
  },
  {
    id: 4,
    title: "Navigating Difficult Conversations as a Leader",
    slug: "navigating-difficult-conversations",
    excerpt: "Practical techniques for approaching challenging discussions with confidence and empathy.",
    content: "",
    image: "https://picsum.photos/id/23/800/500",
    date: "2023-08-22",
    readTime: 5,
    category: "communication",
    author: "Naggib Chakhap"
  },
  {
    id: 5,
    title: "Creating a Culture of Continuous Learning",
    slug: "culture-continuous-learning",
    excerpt: "How to foster an environment where growth and development are prioritized at all levels.",
    content: "",
    image: "https://picsum.photos/id/24/800/500",
    date: "2023-08-05",
    readTime: 9,
    category: "organizational-culture",
    author: "Naggib Chakhap"
  },
  {
    id: 6,
    title: "The Future of Leadership: Trends to Watch",
    slug: "future-leadership-trends",
    excerpt: "Emerging leadership approaches and methodologies that will shape the next decade of management.",
    content: "",
    image: "https://picsum.photos/id/25/800/500",
    date: "2023-07-18",
    readTime: 10,
    category: "leadership",
    author: "Naggib Chakhap"
  }
]

const _categories = [
  { id: "all", name: "All Posts" },
  { id: "leadership", name: "Leadership" },
  { id: "team-building", name: "Team Building" },
  { id: "personal-development", name: "Personal Development" },
  { id: "communication", name: "Communication" },
  { id: "organizational-culture", name: "Organizational Culture" }
]

// State
const selectedCategory = ref("all")
const visiblePosts = ref(6)
const email = ref("")

// Computed
const filteredPosts = computed(() => {
  if (selectedCategory.value === "all" || !selectedCategory.value) {
    return _blogPosts.slice(0, visiblePosts.value)
  }
  return _blogPosts
    .filter(post => post.category === selectedCategory.value)
    .slice(0, visiblePosts.value)
})

const hasMorePosts = computed(() => {
  if (selectedCategory.value === "all" || !selectedCategory.value) {
    return visiblePosts.value < _blogPosts.length
  }
  const categoryPosts = _blogPosts.filter(post => post.category === selectedCategory.value)
  return visiblePosts.value < categoryPosts.length
})

// Methods
const loadMorePosts = () => {
  visiblePosts.value += 3
}

const getCategoryName = (categoryId: string) => {
  const category = _categories.find(cat => cat.id === categoryId)
  return category ? category.name : categoryId
}

const formatDate = (dateString: string) => {
  const options = { year: 'numeric', month: 'long', day: 'numeric' }
  return new Date(dateString).toLocaleDateString('en-US', {
    year: 'numeric', month: 'long', day: 'numeric'
  })
}

const subscribeToNewsletter = () => {
  // Here you would typically send the email to your backend or newsletter service
  alert(`Thank you for subscribing with ${email.value}!`)
  email.value = ""
}
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
