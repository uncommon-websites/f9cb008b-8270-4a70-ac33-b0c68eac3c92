<script lang="ts">
  import Navbar from '$lib/components/Navbar.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import SectionLabel from '$lib/components/SectionLabel.svelte';

  let selectedCategory = $state<string>('all');

  const categories = [
    { id: 'all', label: 'All content' },
    { id: 'stamps', label: 'Stamps' },
    { id: 'coins', label: 'Coins' },
    { id: 'guides', label: 'Guides' }
  ];

  const videos = [
    {
      id: 1,
      title: 'Understanding stamp authentication',
      description: 'Learn the essential techniques experts use to authenticate rare stamps and identify forgeries.',
      duration: '12:34',
      category: 'stamps',
      thumbnail: '/generated/image-hands-examining-a-rare-penny-black-stamp-1765657411180-1.webp'
    },
    {
      id: 2,
      title: 'Ancient coin collecting for beginners',
      description: 'Discover how to start your journey into ancient coin collecting with expert guidance.',
      duration: '18:45',
      category: 'coins',
      thumbnail: '/generated/image-collection-of-ancient-roman-coins-arrang-1765657414303-2.webp'
    },
    {
      id: 3,
      title: 'The authentication process explained',
      description: 'Go behind the scenes with professional appraisers to understand how collectibles are authenticated.',
      duration: '15:20',
      category: 'guides',
      thumbnail: '/generated/image-expert-appraiser-examining-vintage-stamp-1765657416858-3.webp'
    }
  ];

  const articles = [
    {
      id: 1,
      title: 'Getting started with stamp collecting',
      excerpt: 'A comprehensive guide to beginning your stamp collecting journey, from essential tools to building your first collection.',
      readTime: '8 min read',
      category: 'stamps',
      image: '/generated/image-rare-colorful-stamps-from-different-coun-1765657419191-4.webp'
    },
    {
      id: 2,
      title: 'Investing in rare coins: What you need to know',
      excerpt: 'Explore the fundamentals of coin investment, including authentication, grading, and market trends.',
      readTime: '10 min read',
      category: 'coins',
      image: '/generated/image-gold-and-silver-coins-from-various-histo-1765657421681-5.webp'
    },
    {
      id: 3,
      title: 'The complete guide to stamp grading',
      excerpt: 'Understanding the grading system is crucial for collectors. Learn how professionals assess stamp condition and value.',
      readTime: '12 min read',
      category: 'stamps',
      image: '/generated/image-vintage-british-penny-stamps-in-protecti-1765657424550-6.webp'
    },
    {
      id: 4,
      title: 'Essential tools for serious collectors',
      excerpt: 'From magnifying loupes to archival storage, discover the equipment every collector needs to protect and evaluate their investments.',
      readTime: '6 min read',
      category: 'guides',
      image: '/generated/image-collectors-workspace-with-stamps-coins-m-1765657427123-7.webp'
    }
  ];

  let filteredVideos = $derived(
    selectedCategory === 'all' 
      ? videos 
      : videos.filter(v => v.category === selectedCategory)
  );

  let filteredArticles = $derived(
    selectedCategory === 'all' 
      ? articles 
      : articles.filter(a => a.category === selectedCategory)
  );
</script>

<div class="min-h-screen bg-[#f5f5f5] font-sans selection:bg-black selection:text-white">
  <Navbar />
  
  <!-- Hero Section -->
  <section class="bg-[#f5f5f5] px-6 pt-16 pb-12">
    <div class="max-w-[1400px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 mb-16">
        <div class="lg:col-span-8">
          <h1 class="font-serif text-5xl md:text-6xl lg:text-[64px] leading-[1.1] tracking-tight text-gray-900">
            Deepen your expertise in collectibles
          </h1>
        </div>
        <div class="lg:col-span-4 flex flex-col justify-end">
          <p class="text-gray-500 text-lg leading-relaxed">
            Explore our curated collection of articles and videos about stamps, coins, and alternative assets.
          </p>
        </div>
      </div>

      <div class="relative w-full h-[500px] overflow-hidden rounded-sm bg-gray-900">
        <img 
          src="/generated/image-close-up-of-rare-vintage-postage-stamps--1765657408048-0.webp" 
          alt="Rare vintage stamps and collectibles" 
          class="absolute inset-0 w-full h-full object-cover opacity-70"
        />
        <div class="absolute inset-0 bg-gradient-to-tr from-gray-900/60 to-gray-800/30 mix-blend-multiply"></div>
        
        <svg class="absolute inset-0 w-full h-full pointer-events-none" viewBox="0 0 1400 500" fill="none" preserveAspectRatio="none">
          <path d="M-100,500 C200,400 400,80 1500,40" stroke="white" stroke-width="1.5" stroke-opacity="0.3" vector-effect="non-scaling-stroke" />
          <path d="M-100,500 C300,350 600,180 1500,250" stroke="white" stroke-width="1" stroke-opacity="0.1" vector-effect="non-scaling-stroke" />
        </svg>

        <div class="absolute inset-0 flex items-center justify-center">
          <div class="flex items-center gap-2 text-white/90 text-[10px] tracking-[0.2em] font-medium uppercase">
            <div class="w-[2px] h-3 bg-white/90"></div>
            Educational Resources
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Category Filter -->
  <section class="bg-[#f5f5f5] px-6 py-8 border-b border-gray-200">
    <div class="max-w-[1400px] mx-auto">
      <div class="flex flex-wrap gap-3">
        {#each categories as category}
          <button
            onclick={() => selectedCategory = category.id}
            class={[
              'px-5 py-2 rounded text-sm font-medium transition-colors',
              selectedCategory === category.id 
                ? 'bg-black text-white' 
                : 'bg-white text-gray-600 hover:bg-gray-100 border border-gray-200'
            ]}
          >
            {category.label}
          </button>
        {/each}
      </div>
    </div>
  </section>

  <!-- Videos Section -->
  <section class="bg-[#f5f5f5] px-6 py-24">
    <div class="max-w-[1400px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 mb-12">
        <div class="lg:col-span-3">
          <SectionLabel label="Videos" />
        </div>
        <div class="lg:col-span-9">
          <h2 class="font-serif text-3xl md:text-4xl leading-tight text-gray-900">
            Watch and learn from experts
          </h2>
        </div>
      </div>

      {#if filteredVideos.length > 0}
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          {#each filteredVideos as video (video.id)}
            <a href="/" class="group">
              <div class="relative w-full aspect-video overflow-hidden rounded-sm bg-gray-900 mb-4">
                <img 
                  src={video.thumbnail} 
                  alt={video.title}
                  class="absolute inset-0 w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
                />
                <div class="absolute inset-0 bg-black/20 group-hover:bg-black/30 transition-colors"></div>
                
                <div class="absolute inset-0 flex items-center justify-center">
                  <div class="w-16 h-16 rounded-full bg-white/90 flex items-center justify-center group-hover:bg-white transition-colors">
                    <svg class="w-6 h-6 text-black ml-1" fill="currentColor" viewBox="0 0 24 24">
                      <path d="M8 5v14l11-7z"/>
                    </svg>
                  </div>
                </div>

                <div class="absolute bottom-3 right-3 bg-black/80 text-white text-xs px-2 py-1 rounded flex items-center gap-1">
                  <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <circle cx="12" cy="12" r="10"/>
                    <path d="M12 6v6l4 2"/>
                  </svg>
                  {video.duration}
                </div>
              </div>

              <h3 class="font-serif text-xl text-gray-900 mb-2 group-hover:text-gray-600 transition-colors">
                {video.title}
              </h3>
              <p class="text-gray-500 text-sm leading-relaxed">
                {video.description}
              </p>
            </a>
          {/each}
        </div>
      {:else}
        <div class="text-center py-16">
          <p class="text-gray-500">No videos found in this category.</p>
        </div>
      {/if}
    </div>
  </section>

  <!-- Articles Section -->
  <section class="bg-white px-6 py-24">
    <div class="max-w-[1400px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 mb-12">
        <div class="lg:col-span-3">
          <SectionLabel label="Articles" />
        </div>
        <div class="lg:col-span-9">
          <h2 class="font-serif text-3xl md:text-4xl leading-tight text-gray-900">
            In-depth guides and insights
          </h2>
        </div>
      </div>

      {#if filteredArticles.length > 0}
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          {#each filteredArticles as article (article.id)}
            <a href="/" class="group">
              <div class="relative w-full aspect-[4/3] overflow-hidden rounded-sm bg-gray-100 mb-4">
                <img 
                  src={article.image} 
                  alt={article.title}
                  class="absolute inset-0 w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
                />
              </div>

              <div class="flex items-center gap-2 text-xs text-gray-500 mb-3">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/>
                </svg>
                {article.readTime}
              </div>

              <h3 class="font-serif text-2xl text-gray-900 mb-3 group-hover:text-gray-600 transition-colors">
                {article.title}
              </h3>
              <p class="text-gray-500 leading-relaxed">
                {article.excerpt}
              </p>
            </a>
          {/each}
        </div>
      {:else}
        <div class="text-center py-16">
          <p class="text-gray-500">No articles found in this category.</p>
        </div>
      {/if}
    </div>
  </section>

  <!-- CTA Section -->
  <section class="px-6 py-24 bg-[#f5f5f5]">
    <div class="max-w-[1400px] mx-auto text-center">
      <h2 class="font-serif text-3xl md:text-5xl text-gray-900 mb-6 leading-tight">
        Ready to start investing?
      </h2>
      <p class="text-gray-500 text-lg mb-10 max-w-2xl mx-auto leading-relaxed">
        Apply your knowledge and explore our curated collection of authenticated collectibles available for fractional investment.
      </p>
      <a href="/" class="inline-block bg-black text-white px-8 py-4 rounded text-sm font-medium hover:bg-gray-800 transition-colors">
        Browse collectibles
      </a>
    </div>
  </section>

  <Footer />
</div>
