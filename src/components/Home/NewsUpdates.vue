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
          <img :src="post.image" :alt="post.title" class="w-full h-48 object-cover" />

          <div class="p-5">
            <h3 class="text-xl font-semibold text-gray-800 mb-2">{{ post.title }}</h3>
            <p class="text-sm text-gray-500 mb-3">{{ post.date }}</p>
            <p class="text-gray-600 text-sm mb-4">{{ post.excerpt }}</p>
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
    title: "Chitwan Aid Trust Hosts Annual Blood Donation Camp",
    date: "July 25, 2025",
    excerpt: "Over 300 volunteers participated in this year's camp, saving countless lives and raising awareness.",
    link: "#",
    image: "https://images.unsplash.com/photo-1615461066841-8a2291a04b0e?auto=format&fit=crop&w=800&q=80" // blood donation
  },
  {
    title: "Clean Water Initiative Launched in Bharatpur",
    date: "June 18, 2025",
    excerpt: "New water filtration systems are now serving over 1,500 residents in rural communities.",
    link: "#",
    image: "https://images.unsplash.com/photo-1571171637578-41bc2dd41cd2?auto=format&fit=crop&w=800&q=80" // water access
  },
  {
    title: "Digital Literacy Workshop Empowers Women in Chitwan",
    date: "May 5, 2025",
    excerpt: "Women from across the region gained valuable tech skills to boost their confidence and employability.",
    link: "#",
    image: "https://images.unsplash.com/photo-1599059814767-1a9474199b4c?auto=format&fit=crop&w=800&q=80" // women and technology
  },
  {
    title: "Free Health Camp Reaches Remote Villages",
    date: "April 12, 2025",
    excerpt: "Doctors and nurses provided checkups, medicines, and guidance to underserved families.",
    link: "#",
    image: "https://images.unsplash.com/photo-1606240724601-4c769c4a80fc?auto=format&fit=crop&w=800&q=80" // rural health checkup
  }
];

</script>
