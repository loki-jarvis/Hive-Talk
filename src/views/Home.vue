<template>
  <div class="w-full h-screen absolute text-center flex flex-col justify-center items-center bg-gray-100">
    <div class="max-w-3xl mx-auto">
      <h1 class="text-5xl font-bold text-green-600">Hive_Talk</h1>
      <p class="mt-6 text-xl text-gray-500">
        <span ref="typed" class="typed"></span>
      </p>
      <div class="mt-10">
        <router-link tag="button" to="/connect" class="border border-green-600 bg-green-600 hover:bg-transparent text-white font-medium py-3 px-6 rounded-lg shadow-sm hover:shadow-md transition duration-300 ease-in-out">
          Start
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import Typed from "typed.js";

export default {
  mounted() {
    const typed = new Typed(this.$refs.typed, {
      strings: [
        "Real-time Communication between the users over the network. Since this is a web application, users won’t need to install any software but instead login and start using the application."
      ],
      typeSpeed: 50,
      backSpeed: 20,
      backDelay: 1000,
      loop: true,
      showCursor: true,
      cursorChar: "|",
    });
  },
  beforeDestroy() {
    // Destroy typed.js instance on component destroy
    this.typed.destroy();
  },
};
</script>
