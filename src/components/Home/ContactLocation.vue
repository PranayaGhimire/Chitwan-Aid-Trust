<template>
  <section class="bg-white py-16 px-4" id="contact">
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-10">
      <!-- Contact Form -->
      <div>
        <h2 class="text-3xl font-bold mb-6 text-gray-800">Contact Us</h2>
        <form @submit.prevent="handleSubmit" class="space-y-4">
          <input type="text" placeholder="Name" v-model="form.name" class="w-full border p-3 rounded-md" required />
          <input type="email" placeholder="Email" v-model="form.email" class="w-full border p-3 rounded-md" required />
          <input type="text" placeholder="Subject" v-model="form.subject" class="w-full border p-3 rounded-md" required />
          <textarea placeholder="Message" v-model="form.message" rows="5" class="w-full border p-3 rounded-md" required></textarea>
          <button type="submit" class="bg-orange-600 hover:bg-orange-700 text-white px-6 py-3 rounded-md">
            Send Message
          </button>
        </form>
      </div>

      <!-- Contact Info + Map -->
      <div class="space-y-6">
        <h2 class="text-3xl font-bold text-gray-800">Our Office</h2>
        <p class="text-gray-600">Chitwan Aid Trust<br />Official Address: 137 Southcote Lane, RG30 3AJ, Reading, UK</p>
        <p class="text-gray-600">Phone: <a href="tel:+9779812345678" class="text-orange-600 font-medium">07735567548; Surya Bahadur Tamang, General Secretary</a></p>
        <p class="text-gray-600">Email: <a href="mailto:info@chitwanaid.org" class="text-orange-600 font-medium">info@chitwanaid.org</a></p>

        <!-- Social Media with Heroicons -->
        <div class="flex gap-4 text-orange-600 text-2xl mt-4">
          <a href="#" aria-label="Facebook" class="hover:text-orange-800">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M22 12.07C22 6.477 17.523 2 12 2S2 6.477 2 12.07c0 5.047 3.657 9.237 8.438 9.937v-7.03H7.898v-2.907h2.54v-2.217c0-2.507 1.492-3.89 3.777-3.89 1.094 0 2.238.196 2.238.196v2.46h-1.26c-1.243 0-1.63.772-1.63 1.562v1.89h2.773l-.443 2.907h-2.33v7.03C18.343 21.308 22 17.117 22 12.07Z"/>
            </svg>
          </a>
          <a href="#" aria-label="Twitter" class="hover:text-orange-800">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M19.633 7.997c.013.18.013.361.013.541 0 5.522-4.205 11.887-11.887 11.887A11.82 11.82 0 0 1 2 18.29c.42.049.827.062 1.26.062a8.38 8.38 0 0 0 5.188-1.789 4.18 4.18 0 0 1-3.905-2.897c.26.037.52.062.793.062.377 0 .754-.05 1.104-.143a4.174 4.174 0 0 1-3.346-4.096v-.05c.56.31 1.2.497 1.887.52A4.163 4.163 0 0 1 4.58 5.72a11.83 11.83 0 0 0 8.593 4.356 4.708 4.708 0 0 1-.104-.956A4.176 4.176 0 0 1 17.246 5c1.205 0 2.292.507 3.056 1.318a8.252 8.252 0 0 0 2.65-1.01 4.15 4.15 0 0 1-1.83 2.308 8.35 8.35 0 0 0 2.398-.65 8.919 8.919 0 0 1-2.187 2.28Z"/>
            </svg>
          </a>
          <a href="#" aria-label="Instagram" class="hover:text-orange-800">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M7.75 2A5.75 5.75 0 0 0 2 7.75v8.5A5.75 5.75 0 0 0 7.75 22h8.5A5.75 5.75 0 0 0 22 16.25v-8.5A5.75 5.75 0 0 0 16.25 2h-8.5Zm0 1.5h8.5A4.25 4.25 0 0 1 20.5 7.75v8.5A4.25 4.25 0 0 1 16.25 20.5h-8.5A4.25 4.25 0 0 1 3.5 16.25v-8.5A4.25 4.25 0 0 1 7.75 3.5ZM18 6.25a.75.75 0 1 0 0 1.5.75.75 0 0 0 0-1.5ZM12 7a5 5 0 1 0 0 10 5 5 0 0 0 0-10Zm0 1.5a3.5 3.5 0 1 1 0 7 3.5 3.5 0 0 1 0-7Z"/>
            </svg>
          </a>
          <a href="#" aria-label="LinkedIn" class="hover:text-orange-800">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M19.25 3A1.75 1.75 0 0 1 21 4.75v14.5A1.75 1.75 0 0 1 19.25 21H4.75A1.75 1.75 0 0 1 3 19.25V4.75A1.75 1.75 0 0 1 4.75 3h14.5ZM8.25 10.25H6.25v7.5h2v-7.5ZM7.25 6.75a1.125 1.125 0 1 0 0 2.25 1.125 1.125 0 0 0 0-2.25Zm10.5 4.86a2.36 2.36 0 0 0-2.36-2.36c-.922 0-1.47.465-1.718.89V10.25h-2v7.5h2v-4.2c0-.539.44-.975.975-.975s.925.436.925.975v4.2h2v-5.69Z"/>
            </svg>
          </a>
        </div>

        <!-- Map -->
        <div class="rounded-md overflow-hidden shadow">
          <iframe
            class="w-full h-64"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2482.958580653355!2d-1.0071810842281812!3d51.44298777962521!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x48769d24cbaf7a6b%3A0x2492fbb82ac8d34e!2s137%20Southcote%20Ln%2C%20Reading%20RG30%203AJ%2C%20UK!5e0!3m2!1sen!2snp!4v1722590635943!5m2!1sen!2snp"
            allowfullscreen=""
            loading="lazy"
          ></iframe>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from "vue";

const form = reactive({
  name: "",
  email: "",
  subject: "",
  message: "",
});

const handleSubmit = () => {
  alert(`Thank you, ${form.name}! Your message has been sent.`);
  form.name = "";
  form.email = "";
  form.subject = "";
  form.message = "";
};
</script>
