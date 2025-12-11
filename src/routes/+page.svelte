<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import Section from "$lib/components/Section.svelte";
  
  const features = [
    "AI-Powered Interviews",
    "Global Talent Matching",
    "Automated Company Outreach",
    "Single Application Process",
    "5,000+ Remote Opportunities"
  ];

  const news = [
    {
      date: "February 2025",
      title: "Mercor Raises $100M Series B at $2B Valuation, Featured in TechCrunch and Bloomberg",
      image: "/generated/image-happy-professional-celebrating-career-su-1765445099037-4.webp"
    },
    {
      date: "January 2025",
      title: "$50 Million Paid Out to Global Talent Through Mercor's Platform",
      image: "/generated/image-young-diverse-professionals-working-toge-1765445101170-5.webp"
    },
    {
      date: "September 2024",
      title: "Forbes Features Mercor's Journey to $250M Valuation and Rapid Growth",
      image: "/generated/image-professional-reading-positive-news-on-la-1765445103342-6.webp"
    }
  ];

  const opportunities = [
    { name: "Expert Model Trainer", desc: "\\$140\\/hour", highlight: true },
    { name: "Medical Intelligence Analyst", desc: "\\$130\\/hour", highlight: true },
    { name: "Legal Intelligence Analyst", desc: "", highlight: true },
    { name: "Senior Software Engineer", desc: "Putting the “square” back", highlight: false },
    { name: "AI\\/ML Engineer", desc: "The Norwegian Wild Reindeer", highlight: false },
    { name: "Full Stack Developer", desc: "International Centre for Cave Art", highlight: false },
    { name: "Data Scientist", desc: "Europe's First Data Scientistwater Restaurant", highlight: false },
    { name: "DevOps Engineer", desc: "The northernmost energy-positive building", highlight: false },
    { name: "Product Manager", desc: "", highlight: true }
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

<main class="pt-32 pb-20 px-5 md:px-10 font-sans text-black selection:bg-gray-200 bg-[#f5f3ef]">
  
  <!-- Hero Headline -->
  <div class="mb-20 md:mb-32 max-w-5xl">
    <h1 class="text-4xl md:text-6xl lg:text-7xl leading-[1.1] font-normal tracking-tight">
      One application. Thousands of elite remote opportunities. AI-powered matching to your dream role.
    </h1>
  </div>

  <!-- Hero Carousel -->
  <div class="mb-32 relative -mx-5 md:-mx-10">
    <div bind:this={carousel} class="flex gap-4 md:gap-8 overflow-x-auto pb-8 snap-x snap-mandatory scrollbar-hide px-5 md:px-10">
      <!-- Left Image (Partial) -->
      <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-diverse-group-of-young-tech-professional-1765445092469-1.webp" alt="Global talent collaboration" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
      
      <!-- Center Image (Main) -->
      <div class="shrink-0 w-[90vw] md:w-[70vw] lg:w-[50vw] snap-center relative">
        <img src="/generated/image-professional-software-developer-working--1765445089616-0.webp" alt="Remote work opportunities" class="w-full h-[400px] md:h-[600px] object-cover" />
        <div class="mt-4">
          <h3 class="text-lg font-medium">Work From Anywhere</h3>
          <p class="text-gray-500 text-lg">Access elite remote opportunities with top companies worldwide</p>
        </div>
      </div>

      <!-- Right Image (Partial) -->
      <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-young-professional-having-video-call-int-1765445094713-2.webp" alt="AI interview process" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
       <!-- Extra Image -->
       <div class="shrink-0 w-[80vw] md:w-[60vw] lg:w-[40vw] snap-center opacity-50 grayscale transition-all hover:grayscale-0 hover:opacity-100">
        <img src="/generated/image-software-engineer-coding-on-multiple-mon-1765445096853-3.webp" alt="Technical opportunities" class="w-full h-[400px] md:h-[600px] object-cover" />
      </div>
    </div>
  </div>

  <!-- How It Works -->
  <Section label="How It Works">
    <div class="flex flex-col border-t border-gray-200">
      {#each features as feature}
        <a href="/" class="py-6 border-b border-gray-200 text-3xl md:text-4xl lg:text-5xl font-normal hover:text-gray-500 transition-colors block">
          {feature}
        </a>
      {/each}
    </div>
  </Section>

  <!-- Company Milestones -->
  <Section label="Company Milestones" link="/" linkText="All updates">
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

  <!-- For Candidates & Companies -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-10 md:gap-20 py-20 md:py-32">
    <div>
      <img src="/generated/image-remote-worker-with-laptop-in-beautiful-h-1765445105463-7.webp" alt="For Candidates" class="w-full aspect-[4/3] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">For Candidates</h3>
      <p class="text-gray-500 text-lg leading-relaxed">
        Take one 20-minute AI interview and get matched with thousands of elite companies. Our candidates see an average 60% salary increase and save hundreds of hours in job searching.
      </p>
    </div>
    <div>
      <img src="/generated/image-hiring-manager-or-tech-lead-reviewing-ca-1765445107708-8.webp" alt="For Companies" class="w-full aspect-[4/3] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">For Companies</h3>
      <p class="text-gray-500 text-lg leading-relaxed">
        Access the world's best AI talent prediction model. We match you with pre-vetted candidates who have the exact skills and experience you need, from our global pool of top 1% talent.
      </p>
    </div>
  </div>

  <!-- Featured Opportunities -->
  <Section label="Featured Opportunities">
    <div class="flex flex-col gap-2">
      {#each opportunities as opportunity}
        <a href="/" class="group block">
          <h3 class="text-3xl md:text-5xl lg:text-6xl font-normal leading-tight">
            <span class="group-hover:underline decoration-1 underline-offset-8">{opportunity.name}</span>
            {#if opportunity.desc}
              <span class="text-gray-300 ml-2 group-hover:text-gray-400 transition-colors">{opportunity.desc}</span>
            {/if}
          </h3>
        </a>
      {/each}
      
      <a href="/" class="inline-flex items-center gap-2 text-lg text-gray-500 mt-12 hover:text-black transition-colors group">
        → <span class="group-hover:translate-x-1 transition-transform">Browse all 5,000+ opportunities</span>
      </a>
    </div>
  </Section>

  <!-- Get Started -->
  <div class="py-20 md:py-32">
    <div class="max-w-xl">
      <img src="/generated/image-confident-young-professional-ready-to-st-1765445109905-9.webp" alt="Get Started" class="w-full aspect-[3/2] object-cover mb-6" />
      <h3 class="text-xl font-medium mb-2">Ready to Find Your Dream Role?</h3>
      <p class="text-gray-500 text-lg mb-6">
        Take our 20-minute AI interview and get instant access to thousands of elite remote opportunities. No more endless applications—just one conversation that opens every door.
      </p>
      <button class="px-8 py-3 bg-black text-white hover:bg-gray-800 transition-colors text-base font-medium">
        Start Your AI Interview →
      </button>
    </div>
  </div>

  <!-- Footer -->
  <footer class="pt-20 border-t border-gray-200">
    <div class="grid grid-cols-1 md:grid-cols-12 gap-10 md:gap-4">
      <!-- Logo Column -->
      <div class="col-span-1 md:col-span-2">
        <svg width="40" height="40" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="4" y="4" width="11" height="11" rx="2" fill="currentColor" />
          <rect x="9" y="9.5" width="10" height="10" rx="2" fill="currentColor" fill-opacity="0.24" />
        </svg>
      </div>

      <!-- Links Columns -->
      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">For Talent</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">How It Works</a></li>
          <li><a href="/" class="hover:text-black">AI Interview</a></li>
          <li><a href="/" class="hover:text-black">Browse Jobs</a></li>
          <li><a href="/" class="hover:text-black">Success Stories</a></li>
          <li><a href="/" class="hover:text-black">Practice Interview</a></li>
          <li><a href="/" class="hover:text-black">FAQ</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">For Companies</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">Hire Talent</a></li>
          <li><a href="/" class="hover:text-black">AI Matching</a></li>
          <li><a href="/" class="hover:text-black">Teams Search</a></li>
          <li><a href="/" class="hover:text-black">Pricing</a></li>
          <li><a href="/" class="hover:text-black">Case Studies</a></li>
        </ul>
      </div>

      <div class="col-span-1 md:col-span-2">
        <h4 class="text-gray-400 mb-6 text-sm">Company</h4>
        <ul class="space-y-2 text-sm text-gray-600">
          <li><a href="/" class="hover:text-black">About</a></li>
          <li><a href="/" class="hover:text-black">Founders</a></li>
          <li><a href="/" class="hover:text-black">News & Press</a></li>
          <li><a href="/" class="hover:text-black">Careers</a></li>
          <li><a href="/" class="hover:text-black">Contact</a></li>
        </ul>
      </div>

      <!-- Search -->
      <div class="col-span-1 md:col-span-4 flex flex-col justify-end">
        <div class="border-b border-gray-200 flex justify-between items-center py-2">
          <input type="text" placeholder="Search opportunities" class="outline-none w-full text-sm placeholder-gray-400" />
          <span class="text-gray-400">+</span>
        </div>
      </div>
    </div>

    <!-- Bottom Footer -->
    <div class="mt-20 py-8 flex flex-col md:flex-row justify-between items-start md:items-center text-xs text-gray-500 gap-4">
      <div>© Mercor 2025</div>
      
      <a href="/" class="flex items-center gap-1 hover:text-black">
        ↗ We're Hiring
      </a>

      <div class="flex gap-6">
        <a href="/" class="hover:text-black">Privacy Policy</a>
        <a href="/" class="hover:text-black">Terms of Service</a>
        <a href="/" class="hover:text-black">Legal</a>
      </div>

      <div class="flex gap-6">
        <a href="/" class="hover:text-black">Twitter</a>
        <a href="/" class="hover:text-black">LinkedIn</a>
        <a href="/" class="hover:text-black">GitHub</a>
      </div>
    </div>
  </footer>

</main>

