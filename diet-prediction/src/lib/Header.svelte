<script lang="ts">
  import { createMeal } from "../store/create";
  export let style: boolean = false;

  function specialChange() {
    if ($createMeal.create == 1) {
      window.scrollTo({
        top: 900,
        behavior: "smooth",
      });
    } else {
      createMeal.set({ create: 1 });
    }
  }
</script>

<nav class="{style ? 'bg-transparent' : 'bg-beige'} pt-12">
  <div class="max-w-screen-xl flex flex-wrap items-center justify-between">
    <button
      on:click={() => {
        createMeal.set({ create: 1 });
      }}
    >
      {#if style}
        <img class="w-20 h-20" alt="" src="src/assets/dnalogo.svg" />
      {:else}
        <img class="w-40 h-30" alt="" src="src/assets/dnalogo.svg" />
      {/if}
    </button>
    <div class="hidden w-full md:block md:w-auto" id="navbar-default">
      <ul
        class="flex font-normal {style
          ? 'text-white'
          : 'text-black'} space-x-16 font-poppins"
      >
        <li>
          <button
            class="{style
              ? 'bg-orange-100 text-[#B45FC1]'
              : 'bg-[#B45FC1] text-white'} px-9 py-4 rounded-full font-bold -mt-4"
            on:click={() => {
              createMeal.set({ create: 3 });
            }}
            aria-current="page"
          >
            Create Meal
          </button>
        </li>
        <li>
          <button
            class="{style
              ? 'bg-orange-100 text-[#B45FC1]'
              : 'bg-[#B45FC1] text-white'} px-9 py-4 rounded-full font-bold -mt-4"
            on:click={() => {
              createMeal.set({ create: 4 });
            }}
          >
            About Us
          </button>
        </li>
        <li>
          <button
            class="{style
              ? 'bg-orange-100 text-[#B45FC1]'
              : 'bg-[#B45FC1] text-white'} px-9 py-4 rounded-full font-bold -mt-4"
            on:click={specialChange}
          >
            Create Diet Plan
          </button>
        </li>
      </ul>
    </div>
  </div>
</nav>
