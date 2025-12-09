<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import Section from "$lib/components/Section.svelte";
  
  const disciplines = [
    "Architecture",
    "Landscape Architecture",
    "Interior Architecture",
    "Product Design",
    "Brand & Experience"
  ];

  const news = [
    {
      date: "08 December 2025",
      title: "The Joslyn Art Museum receives Prix Versailles World Title for Exterior Design",
      image: "https://images.unsplash.com/photo-1629904853716-f004320d874c?q=80&w=1000&auto=format&fit=crop"
    },
    {
      date: "03 December 2025",
      title: "La Nube wins Children in Museums International Award",
      image: "https://images.unsplash.com/photo-1486325212027-8081e485255e?q=80&w=1000&auto=format&fit=crop"
    },
    {
      date: "03 December 2025",
      title: "Joslyn Museum of Art Expansion Receives Top Awards",
      image: "https://images.unsplash.com/photo-1541888946425-d81bb19240f5?q=80&w=1000&auto=format&fit=crop"
    }
  ];

  const projects = [
    { name: "Bibliotheca Alexandrina", desc: "A Library for the World", highlight: true },
    { name: "Norwegian National Opera and Ballet", desc: "", highlight: true },
    { name: "National September 11 Memorial Museum", desc: "", highlight: true },
    { name: "Times Square", desc: "Putting the “square” back", highlight: false },
    { name: "Viewpoint Snøhetta", desc: "The Norwegian Wild Reindeer", highlight: false },
    { name: "Lascaux IV", desc: "International Centre for Cave Art", highlight: false },
    { name: "Under", desc: "Europe's First Underwater Restaurant", highlight: false },
    { name: "Powerhouse Brattørkaia", desc: "The northernmost energy-positive building", highlight: false },
    { name: "King Abdulaziz Centre for World Culture", desc: "", highlight: true }
  ];
  let carousel: HTMLElement;

  import { onMount } from 'svelte';
  
  onMount(() => {
    if (carousel) {
      const centerImage = carousel.children[1] as HTMLElement;
      if (centerImage) {
        const scrollLeft = centerImage.offsetLeft - (carousel.clientWidth - centerImage.clientWidth) / 2;
        carousel.scrollLeft = scrollLeft;
      }
    }
  });
</script>

<Header />

<main class="pt-32 pb-20 px-5 md:px-10 font-sans text-black selection:bg-gray-200">
  
  <!-- Hero Headline -->
  <div class="mb-20 md:mb-32 max-w-5xl">
    <h1 class="text-4xl md:text-6xl lg:text-7xl leading-[1.1] font-normal tracking-tight">
      Snøhetta is a global transdisciplinary practice, working on projects of all scales.
    </h1>
  </div>

  <!-- Hero Carousel -->
  <div class="mb-32 relative -mx-5 md:-mx-10">
    <div bind:this={carousel} class="flex gap-4 md:gap-8 overflow-x-auto pb-8 snap-x snap-mandatory scrollbar-hide px-5 md:px-10">
      <!-- Left Image (Partial) -->
      <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?q=80&w=1600&auto=format&fit=crop" alt="Project" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
      
      <!-- Center Image (Main) -->
      <div class="shrink-0 w-[90vw] md:w-[70vw] lg:w-[50vw] snap-center relative">
        <img src="https://images.unsplash.com/photo-1506157786151-b8491531f063?q=80&w=1600&auto=format&fit=crop" alt="St. Louis Symphony Orchestra" class="w-full h-[400px] md:h-[600px] object-cover" />
        <div class="mt-4">
          <h3 class="text-lg font-medium">St. Louis Symphony Orchestra</h3>
          <p class="text-gray-500 text-lg">A facility to nurture the creative process</p>
        </div>
      </div>

      <!-- Right Image (Partial) -->
      <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?q=80&w=1600&auto=format&fit=crop" alt="Project" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
       <!-- Extra Image -->
       <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="https://images.unsplash.com/photo-1511818966892-d7d671e672a2?q=80&w=1600&auto=format&fit=crop" alt="Project" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
    </div>
  </div>

  <!-- Disciplines -->
  <Section label="Disciplines">
    <div class="flex flex-col border-t border-gray-200">
      {#each disciplines as discipline}
        <a href="/" class="py-6 border-b border-gray-200 text-3xl md:text-4xl lg:text-5xl font-normal hover:text-gray-500 transition-colors block">
          {discipline}
        </a>
      {/each}
    </div>
  </Section>

  <!-- Latest News -->
  <Section label="Latest News" link="/" linkText="All articles">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each news as item}
        <article class="group cursor-pointer">
          <div class="overflow-hidden mb-4">
            <img src={item.image} alt={item.title} class="w-full aspect-[4/3] object-cover group-hover:scale-105 transition-transform duration-500" />
          </div>
          <time class="text-gray-500 text-sm block mb-2">{item.date}</time>
          <h3 class="text-xl leading-snug group-hover:underline decoration-1 underline-offset-4">{item.title}</h3>
        </article>
      {/each}
    </div>
    
    <!-- Navigation Arrows -->
    <div class="flex justify-between mt-12 border-t border-transparent">
      <button class="hover:opacity-50 transition-opacity p-2 -ml-2">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M19 12H5M12 19l-7-7 7-7"/>
        </svg>
      </button>
      <button class="hover:opacity-50 transition-opacity p-2 -mr-2">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M5 12h14M12 5l7 7-7 7"/>
        </svg>
      </button>
    </div>
  </Section>

  <!-- Process & Sustainability -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-10 md:gap-20 py-20 md:py-32">
    <div>
      <img src="https://images.unsplash.com/photo-1503387762-592deb58ef4e?q=80&w=1200&auto=format&fit=crop" alt="Our process" class="w-full aspect-[4/3] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">Our process</h3>
      <p class="text-gray-500 text-lg leading-relaxed">
        Our unique process has been fine-tuned since our beginnings in 1989. Learn more about our transdisciplinary approach to architecture and design.
      </p>
    </div>
    <div>
      <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=1200&auto=format&fit=crop" alt="Sustainability" class="w-full aspect-[4/3] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">Sustainability and Responsibility</h3>
      <p class="text-gray-500 text-lg leading-relaxed">
        Since our founding in the late 1980s, we have been guided by a deep commitment to environmental and cultural sensitivity.
      </p>
    </div>
  </div>

  <!-- Highlighted Projects -->
  <Section label="Highlighted Projects">
    <div class="flex flex-col gap-2">
      {#each projects as project}
        <a href="/" class="group block">
          <h3 class="text-3xl md:text-5xl lg:text-6xl font-normal leading-tight">
            <span class="group-hover:underline decoration-1 underline-offset-8">{project.name}</span>
            {#if project.desc}
              <span class="text-gray-300 ml-2 group-hover:text-gray-400 transition-colors">{project.desc}</span>
            {/if}
          </h3>
        </a>
      {/each}
      
      <a href="/" class="inline-flex items-center gap-2 text-lg text-gray-500 mt-12 hover:text-black transition-colors group">
        → <span class="group-hover:translate-x-1 transition-transform">See all of our projects</span>
      </a>
    </div>
  </Section>

  <!-- Get in touch -->
  <div class="py-20 md:py-32">
    <div class="max-w-xl">
      <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?q=80&w=1200&auto=format&fit=crop" alt="Get in touch" class="w-full aspect-[3/2] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">Get in touch</h3>
      <p class="text-gray-500 text-lg mb-6">
        We'd love to hear from you. Depending on your inquiry, you'll find the relevant contact details here.
      </p>
      <button class="w-10 h-10 border border-gray-200 flex items-center justify-center hover:bg-black hover:text-white transition-colors">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <line x1="4" y1="21" x2="4" y2="14"></line>
          <line x1="4" y1="10" x2="4" y2="3"></line>
          <line x1="12" y1="21" x2="12" y2="12"></line>
          <line x1="12" y1="8" x2="12" y2="3"></line>
          <line x1="20" y1="21" x2="20" y2="16"></line>
          <line x1="20" y1="12" x2="20" y2="3"></line>
          <line x1="1" y1="14" x2="7" y2="14"></line>
          <line x1="9" y1="8" x2="15" y2="8"></line>
          <line x1="17" y1="16" x2="23" y2="16"></line>
        </svg>
      </button>
    </div>
  </div>

  <!-- Footer -->
  <footer class="pt-20 border-t border-gray-200">
    <div class="grid grid-cols-1 md:grid-cols-12 gap-10 md:gap-4">
      <!-- Logo Column -->
      <div class="col-span-1 md:col-span-2">
        <svg width="40" height="40" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M2 28L10 12L16 24L22 8L30 28" stroke="currentColor" stroke-width="2" stroke-linejoin="round" stroke-linecap="round"/>
        </svg>
      </div>

      <!-- Links Columns -->
      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">General</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">People</a></li>
          <li><a href="/" class="hover:text-black">Process</a></li>
          <li><a href="/" class="hover:text-black">Projects</a></li>
          <li><a href="/" class="hover:text-black">News</a></li>
          <li><a href="/" class="hover:text-black">About</a></li>
          <li><a href="/" class="hover:text-black">Sustainability</a></li>
          <li><a href="/" class="hover:text-black">Perspectives</a></li>
          <li><a href="/" class="hover:text-black">Contact</a></li>
          <li><a href="/" class="hover:text-black">Studios</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">Disciplines</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">Architecture</a></li>
          <li><a href="/" class="hover:text-black">Landscape</a></li>
          <li><a href="/" class="hover:text-black">Interior</a></li>
          <li><a href="/" class="hover:text-black">Product</a></li>
          <li><a href="/" class="hover:text-black">Brand & Experience</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">More</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">Calendar</a></li>
          <li><a href="/" class="hover:text-black">Awards</a></li>
          <li><a href="/" class="hover:text-black">Snøhetta Books</a></li>
        </ul>
      </div>

      <!-- Search -->
      <div class="col-span-1 md:col-span-4 flex flex-col justify-end">
        <div class="border-b border-gray-200 flex justify-between items-center py-2">
          <input type="text" placeholder="Search" class="outline-none w-full text-sm placeholder-gray-400" />
          <span class="text-gray-400">+</span>
        </div>
      </div>
    </div>

    <!-- Bottom Footer -->
    <div class="mt-20 py-8 flex flex-col md:flex-row justify-between items-start md:items-center text-xs text-gray-500 gap-4">
      <div>© Snøhetta 2025</div>
      
      <a href="/" class="flex items-center gap-1 hover:text-black">
        ↗ Current Openings
      </a>

      <div class="flex gap-6">
        <a href="/" class="hover:text-black">Transparency Act</a>
        <a href="/" class="hover:text-black">Cookies & Tracking</a>
        <a href="/" class="hover:text-black">Legal Documents</a>
      </div>

      <div class="flex gap-6">
        <a href="/" class="hover:text-black">Instagram</a>
        <a href="/" class="hover:text-black">Facebook</a>
        <a href="/" class="hover:text-black">LinkedIn</a>
      </div>
    </div>
  </footer>

</main>

