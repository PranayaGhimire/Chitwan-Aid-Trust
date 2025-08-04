<template>
  <section class="bg-white py-16">
    <div class="max-w-6xl mx-auto px-4">
      <h2 class="text-3xl font-bold text-center text-gray-800 mb-10">News & Updates</h2>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(post, index) in newsPosts"
          :key="index"
          class="bg-gray-50 rounded-xl overflow-hidden shadow hover:shadow-lg transition duration-300"
        >
          <img :src="post.image" :alt="post.title" class="w-full h-60 " />

          <div class="p-5">
            <h3 class="text-xl font-semibold text-gray-800 mb-2">{{ post.title }}</h3>
            <p class="text-sm text-gray-500 mb-3">{{ post.date }}</p>
            <a :href="post.link" class="text-orange-600 font-medium hover:underline">Read More →</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const newsPosts = [
  {
    title: "नयॉं सभापतीको चयन",
    date: "July 25, 2025",
    link: "#",
    image: "https://chitwanaidtrust.org/uploads/posts/400x300/post-20.jpg"
  },
  {
    title: "Charity Event",
    date: "June 18, 2025",
    link: "#",
    image: "https://chitwanaidtrust.org/uploads/posts/post-18.jpeg"
  },
  {
    title: "Financial Help - Annapurna High School, Parbatipur",
    date: "May 5, 2025",
    link: "#",
    image: "https://chitwanaidtrust.org/uploads/posts/post-17.jpeg"
  },
  {
    title: "Free Health Camp",
    date: "April 12, 2025",
    link: "#",
    image: "https://chitwanaidtrust.org/uploads/posts/post-16.jpeg"
  }
];

</script>
