<script lang="ts">
  export let label: string = "";
  export let link: string | undefined = undefined;
  export let linkText: string = "";
</script>

<section class="flex flex-col md:flex-row w-full py-12 md:py-20 border-t border-transparent">
  <div class="w-full md:w-1/4 mb-8 md:mb-0 pr-4">
    <h3 class="text-lg text-gray-400 font-normal">{label}</h3>
  </div>
  <div class="w-full md:w-3/4">
    {#if link}
      <div class="flex justify-end mb-8 -mt-10 md:mt-0">
        <a href={link} class="text-lg text-gray-400 hover:text-black transition-colors flex items-center gap-2 group">
          {linkText}
          <span class="group-hover:translate-x-1 transition-transform">→</span>
        </a>
      </div>
    {/if}
    <slot />
  </div>
</section>
