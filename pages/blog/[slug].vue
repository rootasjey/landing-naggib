<template>
  <div class="min-h-screen bg-gray-50 dark:bg-[#11111B]">
    <!-- Hero Section -->
    <div class="-mt-16 bg-gray-50 dark:bg-[#11111B]">
      <div class="h-[60vh] mx-auto flex flex-row justify-center items-center">
        <div class="absolute w-full h-[60vh] bg-black">
          <div class="bg-gradient-to-b from-black to-transparent absolute h-16 w-full z-1"></div>
          <NuxtImg :src="post.image" :alt="post.title" class="w-full h-full absolute object-cover brightness-70" />
        </div>

        <div class="flex flex-col color-white justify-center items-center max-w-4xl text-center z-2 px-4">
          <span class="bg-dark-500 border text-white text-sm px-4 py-1 rounded-full mb-4">
            {{ getCategoryName(post.category) }}
          </span>
          <h1 class="text-4xl md:text-5xl font-700 mb-4">
            {{ post.title }}
          </h1>
          <div class="flex items-center text-gray-300 text-sm">
            <span class="i-ph-user-circle mr-2"></span>
            <span>{{ post.author }}</span>
            <span class="mx-2">•</span>
            <span class="i-ph-calendar mr-2"></span>
            <span>{{ formatDate(post.date) }}</span>
            <span class="mx-2">•</span>
            <span class="i-ph-clock mr-2"></span>
            <span>{{ post.readTime }} min read</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Blog Content Section -->
    <div class="py-16 bg-white dark:bg-[#0D0D17]">
      <div class="container mx-auto px-4">
        <div class="max-w-3xl mx-auto">
          <div class="prose prose-lg dark:prose-invert mx-auto">
            <p class="text-3xl font-600 font-title mb-12 text-gray-700 dark:text-gray-300">
              {{ post.excerpt }}
            </p>
            
            <div v-if="post.content">
              <!-- Actual blog content would be rendered here -->
              <div v-html="post.content"></div>
            </div>
            <div v-else class="flex flex-col gap-8 text-size-8 font-200 color-gray-500">
              <!-- Placeholder content for demo purposes -->
              <p>
                Leadership in the modern workplace requires a unique blend of skills that go beyond traditional management approaches. Today's leaders must navigate complex challenges, from remote work dynamics to rapid technological change.
              </p>
              
              <h2 class="font-600 font-sans color-gray-800 dark:color-gray-200">The Evolving Leadership Landscape</h2>
              <p>
                As organizations become more distributed and diverse, leaders must adapt their approaches to meet new expectations. The command-and-control leadership style of previous generations has given way to more collaborative and empathetic models.
              </p>
              
              <blockquote>
                "The best leaders are those who can inspire their teams while remaining adaptable to changing circumstances."
              </blockquote>
              
              <h2 class="font-600 font-sans color-gray-800 dark:color-gray-200">Key Leadership Competencies</h2>
              <p>
                Based on extensive research and practical experience, these five competencies have emerged as essential for effective leadership:
              </p>
              
              <h3 class="text-size-6 font-400 font-sans color-gray-800 dark:color-gray-200">1. Emotional Intelligence</h3>
              <p>
                The ability to recognize and manage your own emotions, as well as understand and influence the emotions of others, is foundational to modern leadership. Leaders with high emotional intelligence create psychologically safe environments where team members feel valued and understood.
              </p>
              
              <h3 class="text-size-6 font-400 font-sans color-gray-800 dark:color-gray-200">2. Adaptive Thinking</h3>
              <p>
                In a rapidly changing business landscape, leaders must be able to pivot strategies and approaches quickly. This requires comfort with ambiguity and the ability to make decisions with incomplete information.
              </p>
              
              <h3 class="text-size-6 font-400 font-sans color-gray-800 dark:color-gray-200">3. Digital Fluency</h3>
              <p>
                While leaders don't need to be technical experts, they must understand how technology impacts their business and teams. This includes leveraging digital tools for collaboration and staying informed about technological trends that could disrupt their industry.
              </p>
              
              <h3 class="text-size-6 font-400 font-sans color-gray-800 dark:color-gray-200">4. Inclusive Leadership</h3>
              <p>
                Today's diverse workplaces require leaders who can create environments where people of all backgrounds feel welcomed and valued. Inclusive leaders actively seek out different perspectives and ensure all team members have opportunities to contribute.
              </p>
              
              <h3 class="text-size-6 font-400 font-sans color-gray-800 dark:color-gray-200">5. Continuous Learning Mindset</h3>
              <p>
                The pace of change in today's business environment means that leaders must commit to ongoing development. This includes seeking feedback, reflecting on experiences, and actively pursuing new knowledge and skills.
              </p>
              
              <h2 class="font-600 font-sans color-gray-800 dark:color-gray-200">Developing These Skills</h2>
              <p>
                Leadership development is a journey rather than a destination. Here are some strategies for cultivating these essential skills:
              </p>
              
              <ul>
                <li>Seek regular feedback from diverse sources</li>
                <li>Find a mentor or coach who can provide guidance</li>
                <li>Practice self-reflection to identify areas for growth</li>
                <li>Experiment with new approaches in low-risk situations</li>
                <li>Read widely across disciplines to broaden your perspective</li>
              </ul>
              
              <h2 class="font-600 font-sans color-gray-800 dark:color-gray-200">Conclusion</h2>
              <p>
                The leaders who will thrive in the coming years are those who can balance technical expertise with human-centered leadership. By developing these five essential skills, you'll be better positioned to navigate the complexities of the modern workplace and inspire your team to achieve exceptional results.
              </p>
            </div>
            
            <!-- Tags -->
            <div class="mt-12 pt-6 border-t border-gray-200 dark:border-gray-700">
              <div class="flex flex-wrap gap-2">
                <span class="text-sm text-gray-600 dark:text-gray-400 mr-2">Tags:</span>
                <span 
                  v-for="tag in ['Leadership', 'Management', 'Professional Development']" 
                  :key="tag"
                  class="bg-gray-100 dark:bg-[#1A1A2E] text-gray-700 dark:text-gray-300 text-xs px-3 py-1 rounded-full"
                >
                  {{ tag }}
                </span>
              </div>
            </div>
            
            <!-- Author Bio -->
            <div class="mt-12 p-6 bg-gray-50 dark:bg-[#1A1A2E] rounded-lg">
              <div class="flex items-center gap-4">
                <div class="w-24 h-24 flex rounded-full overflow-hidden">
                  <NuxtImg src="/images/naggib-pp.jpeg" alt="Naggib Chakhap" class="w-full h-full object-cover" />
                </div>
                <div>
                  <h4 class="text-lg font-600">{{ post.author }}</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-400 mb-3">
                    Leadership Coach & Consultant
                  </p>
                  <p class="text-sm">
                    Naggib is a leadership coach and consultant with over 20 years of experience helping leaders and organizations reach their full potential.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Related Posts Section -->
    <div class="py-16 bg-gray-50 dark:bg-[#11111B]">
      <div class="container mx-auto px-4">
        <div class="max-w-3xl mx-auto">
          <h2 class="text-2xl font-600 mb-8 text-center">You Might Also Like</h2>
          
          <div class="grid gap-8"
            :class="{
              'grid-cols-1': relatedPosts.length === 1,
              'grid-cols-2': relatedPosts.length === 2,
              'grid-cols-3': relatedPosts.length > 2,
            }"
          >
            <div 
              v-for="relatedPost in relatedPosts" 
              :key="relatedPost.id" 
              class="bg-white dark:bg-[#1A1A2E] rounded-lg overflow-hidden shadow-sm hover:shadow-md transition-all duration-300"
            >
              <NuxtLink :to="`/blog/${relatedPost.slug}`" class="block">
                <div class="relative h-64 overflow-hidden">
                  <NuxtImg 
                    :src="relatedPost.image" 
                    :alt="relatedPost.title" 
                    class="w-full h-full object-cover transition-transform duration-500 hover:scale-105" 
                  />
                </div>
                <div class="p-4">
                  <h3 class="text-lg font-600 mb-2 line-clamp-2">{{ relatedPost.title }}</h3>
                  <div class="flex items-center text-gray-500 dark:text-gray-400 text-xs">
                    <span class="i-ph-calendar mr-1"></span>
                    <span>{{ formatDate(relatedPost.date) }}</span>
                    <span class="mx-2">•</span>
                    <span class="i-ph-clock mr-1"></span>
                    <span>{{ relatedPost.readTime }} min read</span>
                  </div>
                </div>
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CTA Section -->
    <div class="curved py-16 bg-transparent text-center">
      <div class="container mx-auto px-4">
        <h2 class="color-white text-size-4xl font-500 mb-2">
          Ready to elevate your leadership?
        </h2>
        <p class="text-lg text-gray-300 max-w-2xl mx-auto mb-8">
          Take the next step in your leadership journey with personalized coaching and training.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <UButton
            label="Schedule a consultation"
            btn="~"
            rounded="full"
            to="/contact"
            class="mx-auto bg-[#F5C45E] hover:bg-[#F5C45E]/90 text-black font-semibold px-6"
          />
          <UButton
            label="Explore services"
            btn="~"
            rounded="full"
            variant="outline"
            to="/services"
            class="mx-auto color-white dark:border-white dark:text-white font-semibold px-6"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const slug = route.params.slug

// Mock data for blog posts (in a real app, this would come from an API or CMS)
const _blogPosts = [
  {
    id: 1,
    title: "5 Essential Leadership Skills for the Modern Workplace",
    slug: "essential-leadership-skills-modern-workplace",
    excerpt: "Discover the key leadership competencies needed to thrive in today's rapidly evolving business environment.",
    content: "",
    image: "https://picsum.photos/800/500?random=1",
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
    image: "https://picsum.photos/800/500?random=1",
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
    image: "https://picsum.photos/800/500?random=1",
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
    image: "https://picsum.photos/800/500?random=1",
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
    image: "https://picsum.photos/800/500?random=1",
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
    image: "https://picsum.photos/800/500?random=1",
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

// Find the current post based on the slug
const post = computed(() => {
  return _blogPosts.find(post => post.slug === slug) || _blogPosts[0]
})

// Get related posts (excluding the current post)
const relatedPosts = computed(() => {
  return _blogPosts
    .filter(p => p.id !== post.value.id && p.category === post.value.category)
    .slice(0, 2)
})

// Methods
const getCategoryName = (categoryId: string) => {
  const category = _categories.find(cat => cat.id === categoryId)
  return category ? category.name : categoryId
}

const formatDate = (dateString: string) => {
  const options = { year: 'numeric', month: 'long', day: 'numeric' }
  return new Date(dateString).toLocaleDateString('en-US', options as any)
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
      
  background: #000;
  height: calc(var(--size) + 350px);
}
</style>
