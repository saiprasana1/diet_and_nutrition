<script>
  import Connect from "./Connect.svelte";
  import { createMeal } from "../store/create";
</script>

<div class="mt-52">
  <img src="src/assets/dnalogo.svg" alt="Logo again" class="w-40 h-32 mx-auto" />
  <div>
    <ul class="flex font-poppins text-xl space-x-36 justify-center my-10">
      <li>
        <button
          class="border bg-[#B45FC1] font-bold text-orange-100 p-2 rounded"
          on:click={() => {
            createMeal.set({ create: 3 });
            window.scrollTo({
              top: 0,
            });
          }}
        >
          Create Meal
        </button>
      </li>
      <li>
        <button
          class="border bg-[#B45FC1] font-bold text-orange-100 p-2 rounded"
          on:click={() => {
            createMeal.set({ create: 1 });
            window.scrollTo({
              top: 900,
            });
          }}
        >
          Create Diet Plan
        </button>
      </li>
      <li>
        <button
          class="border bg-[#B45FC1] font-bold text-orange-100  p-2 rounded"
          on:click={() => {
            createMeal.set({ create: 4 });
            window.scrollTo({
              top: 0,
            });
          }}
        >
          About Us
        </button>
      </li>
    </ul>
  </div>
  <Connect />
</div>
