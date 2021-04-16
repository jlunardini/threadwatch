<template>
  <div class="w-full h-full flex justify-center items-center flex-col">
    <div class="make-sansita text-6xl text-yellow-600 w-full text-center">
      Welcome to DenimTracker
    </div>
    <div class="flex justify-center space-x-4 mt-8 w-full">
      <p
        class="border-2 p-4 rounded-full text-lg font-semibold hover:border-yellow-600 hover:bg-gray-100"
      >
        Login
      </p>
      <p
        @click="showAbout = 'true'"
        class="border-2 p-4 rounded-full text-lg font-semibold hover:border-yellow-600 hover:bg-gray-100"
      >
        About
      </p>
    </div>
    <template v-if="showAbout">
      <About></About>
    </template>
  </div>
</template>

<script>
import About from "../components/About";
export default {
  data() {
    return {
      showAbout: false,
    };
  },
};
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
