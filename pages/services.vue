<template>
  <div class="min-h-screen bg-gray-50 dark:bg-[#11111B]">
    <!-- Hero Section -->
    <div class="-mt-16 bg-gray-50 dark:bg-[#11111B]">
      <div class="h-screen mx-auto flex flex-row justify-center items-center">
        <div class="absolute w-full h-full bg-black">
          <div class="bg-gradient-to-b from-black to-transparent absolute h-16 w-full z-1"></div>
          <NuxtImg src="/images/mic.jpg" alt="Who I Help" :modifiers="{ blur: 25 }" class="w-full h-full absolute object-cover brightness-70" />
        </div>

        <div class="flex flex-col color-white justify-center items-center max-w-4xl text-center z-2">
          <h1 class="mt-6 font-body text-size-20 font-500 uppercase">
            My services
          </h1>
          <p class="text-lg font-400 max-w-500px">
            Elevate Your Leadership Journey. 
            Transform your leadership capabilities,
            empower your team, and drive organizational success.
          </p>
          <div class="flex gap-6 mt-12">
            <NuxtLink to="#coaching-section" class="relative">
              <div class="shadow-md rounded-2 w-40 h-40 hover:scale-105 hover:shadow-primary/20 hover:shadow-lg transition-all duration-500 relative overflow-hidden group">
                <NuxtImg src="/images/service-coaching.webp" alt="Small business owners" class="w-40 h-40 object-cover brightness-90 rounded-2" />
              </div>
              <h3 class="w-full p-2">Coaching</h3>
            </NuxtLink>

            <NuxtLink to="#corporate-training-section" class="relative">
              <div class="shadow-md rounded-2 w-40 h-40 hover:scale-105 hover:shadow-primary/20 hover:shadow-lg transition-all duration-500 relative overflow-hidden group">
                <NuxtImg src="/images/corporate-paper.jpg" alt="Non-profit organizations" class="w-40 h-40 object-cover brightness-90 rounded-2" />
              </div>
              <h3 class="w-full p-2">Corporate training</h3>
            </NuxtLink>

            <NuxtLink to="#keynote-speaking-section" class="relative">
              <div class="shadow-md rounded-2 w-40 h-40 hover:scale-105 hover:shadow-primary/20 hover:shadow-lg transition-all duration-500 relative overflow-hidden group">
                <NuxtImg src="/images/mic.jpg" alt="Executive & first-time leaders" class="w-40 h-40 object-cover brightness-90 rounded-2" />
              </div>
              <h3 class="w-full p-2">Keynote speaking</h3>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>

    <!-- Coaching Section -->
    <div id="coaching-section" class="py-16 bg-white dark:bg-[#0D0D17]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Getting perspective</h3>
          <h2 class="text-size-12 font-100 dark:text-color-gray-400">
            Coaching
          </h2>
        </div>

        <div class="max-w-3xl mx-auto">
          <div class="flex flex-col gap-8 
            font-text font-300 text-size-8 prose prose-lg dark:prose-invert mx-auto"
          >
            <NuxtImg 
              src="/images/service-coaching.webp" alt="Coaching" 
              width="300" 
              class="rounded-lg mx-auto" 
            />

            <p>
              I am an experienced executive coach, leadership development consultant and corporate trainer with over 20 years international experience of leading and building highly effective teams.
            </p>

            <div class="my-12 dark:bg-[#1A1A2E] p-6  border b-dashed flex flex-col items-center rounded-lg">
              <h4 class="font-600 text-size-6">A process for success, made easy</h4>
              <div class="flex gap-14 text-size-6 font-200 mt-12">
                <div class="flex flex-col items-center gap-2">
                  <span class="i-ph-list"></span>
                  <span>Define your goals</span>
                </div>
                <div class="flex flex-col items-center gap-2">
                  <span class="i-ph-path"></span>
                  <span>Follow the steps</span>
                </div>
                <div class="flex flex-col items-center gap-2">
                  <span class="i-ph-target"></span>
                  <span>Meet your potential</span>
                </div>
              </div>
            </div>

            <p>
              What if you could wake up every morning over the next year 
              with a clear roadmap to achieve your desired life? 
            </p>
            
            <p>
              Many people start each year with vague aspirations for change, 
              and end it feeling unsure if they made any progress and wondering what went wrong. 
              The reality is, we can all fall into this trap. 
            </p>
            
            <p>
              It is only with an effective understanding of your goals, 
              a grasp of your biggest blockers 
              and a clear trajectory of how will you get from start to finish that you can achieve 
              the success you desire.
            </p>
            
            <p>
              My coaching services will help you to realise this potential.
            </p>

            <div class="my-12 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="font-600 text-size-6 mb-4">What you will achieve:</h4>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Preparation for role / career change or a promotion</li>
                <li>Methods of managing stress, change, conflict or crisis</li>
                <li>Enhancing personal impact and performance</li>
                <li>Identifying solutions to specific work-related issues</li>
                <li>Increased openness to personal learning and development</li>
                <li>Coaching will get you further and faster than doing it on your own</li>
              </ul>
            </div>

            <p>
              Whether you're a new manager stepping into leadership or a seasoned executive looking to refine your approach, my coaching provides a safe space to explore challenges, develop new skills, and achieve breakthrough results.
            </p>

            <div class="my-12 flex flex-col items-center bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="font-600 text-size-6">Coaching to meet every need and circumstance</h4>
              <div class="mt-12 w-full flex flex-wrap justify-center gap-2 items-center">
                <div v-for="(relationType, index) in _relationTypes" :key="index" 
                  class="w-49 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 flex flex-col
                  border border-dashed border-gray-300 dark:border-gray-700
                  cursor-pointer hover:scale-101 active:scale-99 transition-all duration-300
                  hover:border-solid hover:border-primary-500
                  flex justify-center items-center"
                >
                  <span :class="relationType.icon" class="text-size-4 font-700 bg-primary-500 text-white rounded-full w-6 h-6 flex justify-center items-center" />

                  <div class="text-center flex flex-col">
                    <h3 class="text-size-6 font-800">{{ relationType.name }}</h3>
                    <p class="mt-4 text-sm text-gray-600 dark:text-gray-400">
                      {{ relationType.description }}
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Corporate Training Section -->
    <div id="corporate-training-section" class="py-16  bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Take your team to the next level</h3>
          <h2 class="text-size-12 font-100 text-color-gray-700 dark:text-color-gray-400">
            Corporate Training
          </h2>
        </div>

        <div class="max-w-3xl mx-auto">
          <div class="flex flex-col gap-8 
            font-text font-300 text-size-8 prose prose-lg dark:prose-invert mx-auto"
          >
            <p>
              I understand that employee development is essential for any organisation's success. 
              I offer a comprehensive range of training programs 
              that are specifically designed to help businesses of all sizes achieve their goals. 
            </p>
            <p>
              My corporate training services are designed to enhance employee skills, 
              improve productivity, and increase overall job satisfaction. 
              I will work with you to identify your organisation's specific concerns 
              and create customised training programs that deliver measurable results. 
            </p>

            <div class="bg-[#FAFAF9] dark:bg-[#1A1A2E] py-12 rounded-2 mt-12 w-full flex flex-wrap justify-center gap-2 items-center">
              <div v-for="(trainingType, index) in _trainingTypes" :key="index" 
                class="w-68 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 flex flex-col
                border border-dashed border-gray-300 dark:border-gray-700
                cursor-pointer hover:scale-101 active:scale-99 transition-all duration-300
                hover:border-solid hover:border-primary-500
                flex justify-center items-center"
              >
                <span :class="trainingType.icon" class="text-size-4 font-700 bg-primary-500 text-white rounded-full w-6 h-6 flex justify-center items-center" />

                <div class="text-center flex flex-col">
                  <h3 class="font-800">{{ trainingType.name }}</h3>
                  <p class="mt-6 text-sm text-gray-600 dark:text-gray-400">
                    {{ trainingType.description }}
                  </p>
                </div>
              </div>
            </div>

            <p>
              Whether you are looking to train new employees, 
              upskill your current workforce, or enhance leadership skills, 
              I have the expertise and resources to help you achieve your objectives.
            </p>

            <div class="my-12 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="font-600 text-size-6 mb-4">What you will achieve:</h4>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Improved productivity and efficiency</li>
                <li>Increased job satisfaction and morale</li>
                <li>Enhancing competitiveness</li>
                <li>Improved customer satisfaction</li>
                <li>Reduced employee turnover</li>
                <li>Improved safety</li>
                <li>Adaptability to change</li>
                <li>Enhanced innovation and creativity</li>
                <li>Compliance with regulations and standards</li>
                <li>Improved leadership and management</li>
              </ul>
            </div>

            <div class="mt-2 text-size-5">
              <UAccordion :items="_faqTrainingItems" />
            </div>

            <p>
              All training programs are customized to address your organization's specific challenges and goals, with practical tools that participants can implement immediately.
            </p>

            <div class="border b-dashed p-6 rounded-2 grid md:grid-cols-2 gap-4 text-size-4">
              <div class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-md">
                <h4 class="font-600 mb-3">Leadership Development</h4>
                <p class="text-gray-700 dark:text-gray-300">
                  Comprehensive programs to develop leadership capabilities across your organization, from emerging leaders to executive teams.
                </p>
              </div>

              <div class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-md">
                <h4 class="font-600 mb-3">Team Effectiveness</h4>
                <p class="text-gray-700 dark:text-gray-300">
                  Build high-performing teams through improved communication, conflict resolution, and collaborative problem-solving.
                </p>
              </div>

              <div class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-md">
                <h4 class="font-600 mb-3">Change Management</h4>
                <p class="text-gray-700 dark:text-gray-300">
                  Navigate organizational transitions with strategies that minimize disruption and maximize buy-in from all stakeholders.
                </p>
              </div>
              
              <div class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-md">
                <h4 class="font-600 mb-3">Emotional Intelligence</h4>
                <p class="text-gray-700 dark:text-gray-300">
                  Develop self-awareness and interpersonal skills that enhance leadership effectiveness and team dynamics.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Keynote Speaking Section -->
    <div id="keynote-speaking-section" class="py-16 bg-white dark:bg-[#0D0D17]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Make your event stand out</h3>
          <h2 class="text-size-12 font-100 dark:text-color-gray-400">
            Keynote Speaking
          </h2>
        </div>

        <div class="max-w-3xl mx-auto">
          <div class="flex flex-col gap-8 
            font-text font-300 text-size-8 prose prose-lg dark:prose-invert mx-auto"
          >
            <p>
              Energize your events with thought-provoking keynotes that combine practical leadership insights with engaging storytelling and actionable takeaways.
            </p>

            <div class="bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="text-size-6 font-600 mb-6">Popular Speaking Topics:</h4>
              <ul class="list-disc text-size-4 pl-6 space-y-3">
                <li>
                  <p class="font-600">Finding Your Leadership Sweet Spot</p>
                  <p class="text-sm text-gray-600 dark:text-gray-400 mt-1">
                    Discover how to align your purpose, passion, and skills to lead with authenticity and impact.
                  </p>
                </li>
                <li>
                  <p class="font-600">Leading Through Uncertainty</p>
                  <p class="text-sm text-gray-600 dark:text-gray-400 mt-1">
                    Strategies for maintaining team cohesion and forward momentum during times of change and challenge.
                  </p>
                </li>
                <li>
                  <p class="font-600">The Balanced Leader</p>
                  <p class="text-sm text-gray-600 dark:text-gray-400 mt-1">
                    How to achieve professional success without sacrificing personal fulfillment and well-being.
                  </p>
                </li>
              </ul>
            </div>

            <p>
              Are you looking for a keynote speaker who can inspire and captivate your audience? <br/> 
              I am a renowned public speaker who specializes in delivering impactful and engaging keynote speeches. 
            </p>


            <div class="my-6 bg-gray-50 dark:bg-[#1A1A2E] p-6 rounded-lg">
              <h4 class="font-600 text-size-6 mb-4">My keynote speeches help deliver:</h4>
              <ul class="list-disc text-size-4 font-300 pl-6 space-y-2">
                <li>Receive an inspirational message</li>
                <li>Increase event engagement</li>
                <li>Find networking opportunities</li>
                <li>Improve education and learning</li>
                <li>A memorable experience</li>
              </ul>
            </div>
            
            <p>
              With years of experience in various industries and a passion for motivating others, 
              I have become a sought-after keynote speaker for conferences, corporate events, and other occasions. 
            </p>

            <p>
              Whether you need a keynote speaker to kick off your event 
              or to provide a memorable closing message, 
              I can deliver a speech that will leave your audience inspired, 
              energised, and motivated to take action.
            </p>

            <div class="bg-[#FAFAF9] dark:bg-[#1A1A2E] py-12 rounded-2 mt-12 w-full flex flex-wrap justify-center gap-2 items-center">
              <div v-for="(speechType, index) in _speechTypes" :key="index" 
                class="w-68 bg-[#F8F8F8] dark:bg-[#11111B] rounded-2 relative p-4 flex flex-col
                border border-dashed border-gray-300 dark:border-gray-700
                cursor-pointer hover:scale-101 active:scale-99 transition-all duration-300
                hover:border-solid hover:border-primary-500
                flex justify-center items-center"
              >
                <span :class="speechType.icon" class="text-size-4 font-700 bg-primary-500 text-white rounded-full w-6 h-6 flex justify-center items-center" />

                <div class="text-center flex flex-col">
                  <h3 class="font-800">{{ speechType.name }}</h3>
                  <p class="mt-6 text-sm text-gray-600 dark:text-gray-400">
                    {{ speechType.description }}
                  </p>
                </div>
              </div>
            </div>

            <p>
              Each presentation is tailored to your audience and event objectives, delivering a memorable experience that inspires meaningful action and lasting change.
            </p>

            <div class="mt-2 text-size-5">
              <UAccordion :items="_faqSpeechItems" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Testimonials Section -->
    <div class="py-16 bg-[#F8F8F8] dark:bg-[#11111B]">
      <div class="container mx-auto px-4">
        <div class="flex flex-col justify-center items-center w-full mb-12">
          <span>•</span>
          <h3 class="uppercase font-700">Client Success</h3>
          <h2 class="text-size-12 font-100 text-color-gray-700 dark:text-color-gray-400">
            What Leaders Say
          </h2>
        </div>
        
        <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-8">
          <div v-for="(testimonial, index) in _testimonials" :key="index" 
            class="bg-white dark:bg-[#1A1A2E] p-6 rounded-lg shadow-sm
             flex flex-col justify-between">
            <p class="italic text-gray-700 dark:text-gray-300 mb-4">
              ”{{ testimonial.review }}”
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
          Ready to take the next step?
        </h2>
        <p class="text-lg text-gray-300 max-w-2xl mx-auto mb-8">
          Let's discuss how my services can be tailored to meet your specific leadership development needs.
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
            label="View programs"
            btn="~"
            rounded="full"
            variant="outline"
            to="#"
            class="mx-auto color-white dark:border-[#3A59D1] dark:text-[#3A59D1] dark:border-white dark:text-white font-semibold px-6"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

const _faqSpeechItems = [
  {
    label: "What is a keynote speech?",
    content: "A keynote speech is a talk given during an event that helps to set the tone for the rest of the event. It is typically delivered by a seasoned speaker who has expertise in a particular subject.",
    defaultOpen: true,
  },
  {
    label: "How long do your speeches last?",
    content: "The length of a keynote speech can vary depending on the event and the topic covered. Typically, my keynote speeches last between 30 minutes to an hour.",
  },
  {
    label: "What topics do you typically cover in your speeches?",
    content: "I  can cover a wide range of topics, depending on the theme of the event. Some common topics include leadership, motivation, innovation, teamwork, and personal development.",
  },
]

const _faqTrainingItems = [
  {
    label: "What type of training do you offer?",
    content: "I offer a wide range of training programs, including leadership development, customer service, communication skills, diversity and inclusion, workplace safety, and more. I can also create bespoke programs tailored to your company’s specific needs and goals.",
    defaultOpen: true,
  },
  {
    label: "How do you measure the effectiveness of your training programs?",
    content: "I use a variety of methods to measure the effectiveness of our training programs, including pre- and post-training assessments, feedback surveys, and follow-up evaluations. I also work closely with our clients to identify key performance indicators and track progress over time.",
  },
  {
    label: "How do you ensure that training is engaging and relevant to our employees?",
    content: "I use a variety of techniques to ensure that our training programs are engaging and relevant to your employees, including interactive exercises, case studies, and real-world examples. I also work closely with my clients to understand their unique culture and challenges, and tailor my programs accordingly.",
  },
  {
    label: "What qualifications do you have?",
    content: "I am a highly qualified professional with extensive experience in the coaching, mentoring and training spaces. I stay up-to-date on the latest trends and best practices through ongoing professional development. I have over 4,000 hours of coaching executives and leaders of multinational businesses, non-profit organisations and entrepreneurs. I have an advanced degree (MBA) and additional certifications from: EMCC, Maxwell Leadership Certified Coach, AoEC (Academy of Executive Coaching), DISC Human Behaviour Consultant.",
  },
  {
    label: "Can you provide training remotely or in-person?",
    content: "Yes, I offer both remote and in-person training options, depending on your needs and preferences. We use state-of-the-art technology to deliver remote training that is just as engaging and effective as in-person training, while also offering the convenience and flexibility of remote learning.",
  }
]

const _relationTypes = [
  {
    name: "One-to-one",
    icon: "i-ph-person",
    description: "One-to-one coaching is a personalised approach where I work closely with you to help you achieve your goals by providing guidance, feedback, and support tailored to your specific needs."
  },
  {
    name: "Workshops",
    icon: "i-icon-park-outline-peoples-two",
    description: "Group coaching and workshops are interactive and collaborative learning experiences designed to facilitate personal and professional growth through group discussions, activities, and exercises."
  },
  {
    name: "Online",
    icon: "i-ph-monitor",
    description: "Online coaching is a flexible format that leverages digital platforms to connect coaches and clients remotely, allowing for easy scheduling, accessibility, and efficient communication."
  },
]

const _trainingTypes = [
  {
    name: "Standard training",
    icon: "i-ph-cube-duotone",
    description: "I offer ready-made solutions for common training needs, such as customer service, workplace safety, and communication skills. These programs are expertly designed and can be quickly implemented to improve employee skills and performance."
  },
  {
    name: "Bespoke training",
    icon: "i-ph-hammer-duotone",
    description: "My tailored training packages are developed around your unique needs and goals. I work with you to develop a program that addresses your specific challenges with measurable results that will lead you and your team to success. Team play is the key to success."
  },
]

const _speechTypes = [
  {
    name: "Standard speech",
    icon: "i-ph-microphone-stage-duotone",
    description: "My flagship speeches are a fantastic, cost-effective option for any event. Whilst written in advance, they are designed to be applicable to a broad range of audiences and events. I can typically deliver these speeches at shorter notice."
  },
  {
    name: "Bespoke speech",
    icon: "i-icon-park-outline-microphone-one",
    description: "If you need something more tailored to specific subject or audience, my tailor-made speeches are a great option. These can often lead to a more impactful and memorable experience for attendees and a greater return on investment for you."
  },
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
