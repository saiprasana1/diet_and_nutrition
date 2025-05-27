<script lang="ts">
  import Calculator from "./Calculator.svelte";
  import Header from "./Header.svelte";
  import Landing from "./Landing.svelte";
  import Footer from "./Footer.svelte";
</script>

<div class=" mx-16">
  <Header />
  <Landing />
</div>
<div id="calulator">
  <Calculator />
</div>
<div>
  <a
    href="https://chatbot-khaki-three.vercel.app/"
    target="_blank"
    aria-label="Go to Fitness Chatbot"
    class="fixed bottom-5 right-5 z-50  hover:bg-white hover:shadow-purple-700 text-white text-3xl rounded-full p-4 shadow-lg"
  >
    🤖
  </a>  
</div>
<div>
  <Footer />
</div>
