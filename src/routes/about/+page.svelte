<script lang="ts">
  import Navbar from '$lib/components/Navbar.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import SectionLabel from '$lib/components/SectionLabel.svelte';
</script>

<div class="min-h-screen bg-[#f5f5f5] font-sans selection:bg-black selection:text-white">
  <Navbar />
  
  <!-- Hero Section -->
  <section class="bg-[#f5f5f5] px-6 pt-16 pb-12">
    <div class="max-w-[1400px] mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 mb-16">
        <div class="lg:col-span-8">
          <h1 class="font-serif text-5xl md:text-6xl lg:text-[64px] leading-[1.1] tracking-tight text-gray-900">
            Democratizing access to authenticated collectibles
          </h1>
        </div>
        <div class="lg:col-span-4 flex flex-col justify-end">
          <p class="text-gray-500 text-lg leading-relaxed">
            We're building the future of alternative asset investing, making institutional-grade collectibles accessible to everyone.
          </p>
        </div>
      </div>

      <div class="relative w-full h-[500px] overflow-hidden rounded-sm bg-gray-900">
        <img 
          src="/generated/image-professional-wealth-managers-and-collect-1765650888310-1.webp" 
          alt="Censta team and collectibles" 
          class="absolute inset-0 w-full h-full object-cover opacity-60"
        />
        <div class="absolute inset-0 bg-gradient-to-tr from-gray-900/70 to-gray-800/40 mix-blend-multiply"></div>
        
        <svg class="absolute inset-0 w-full h-full pointer-events-none" viewBox="0 0 1400 500" fill="none" preserveAspectRatio="none">
          <path d="M-100,500 C200,400 400,80 1500,40" stroke="white" stroke-width="1.5" stroke-opacity="0.3" vector-effect="non-scaling-stroke" />
          <path d="M-100,500 C300,350 600,180 1500,250" stroke="white" stroke-width="1" stroke-opacity="0.1" vector-effect="non-scaling-stroke" />
        </svg>

        <div class="absolute inset-0 flex items-center justify-center">
          <div class="flex items-center gap-2 text-white/80 text-[10px] tracking-[0.2em] font-medium uppercase">
            <div class="w-[2px] h-3 bg-white/80"></div>
            Est 2024
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Story Section (v1) -->
  <section class="bg-[#f5f5f5] px-6 py-24">
    <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-12 gap-12">
      <div class="lg:col-span-3">
        <SectionLabel label="Our Story" />
      </div>
      
      <div class="lg:col-span-9 space-y-16">
        <!-- Story Introduction -->
        <div>
          <h2 class="font-serif text-3xl md:text-4xl leading-tight text-gray-900 mb-6">
            Built by collectors, for collectors
          </h2>
          <p class="text-gray-500 text-lg leading-relaxed mb-6">
            Kupa Pounsford and Joshua Rudland-Potter founded Censta to democratize access to authenticated alternative assets, bringing institutional-grade collectibles investing to affluent millennials and wealth managers.
          </p>
          <p class="text-gray-500 leading-relaxed">
            The idea was born from a simple observation: the $370B alternative assets market remained largely inaccessible to those who could benefit most from portfolio diversification. Traditional barriers—authentication concerns, high minimum investments, and lack of liquidity—kept passionate collectors and savvy investors on the sidelines.
          </p>
        </div>

        <!-- The Challenge -->
        <div class="border-l-2 border-gray-200 pl-8">
          <h3 class="font-serif text-2xl text-gray-900 mb-4">
            The challenge we saw
          </h3>
          <p class="text-gray-500 leading-relaxed mb-4">
            Affluent millennials were seeking portfolio diversification beyond traditional stocks and bonds, but lacked access to authenticated alternative assets. Wealth managers struggled to offer their clients tangible, appreciating assets with transparent secondary market access.
          </p>
          <p class="text-gray-500 leading-relaxed">
            Meanwhile, the collectibles market remained fragmented, opaque, and dominated by high-net-worth individuals with deep expertise and connections. Authentication was inconsistent, pricing was unclear, and liquidity was virtually nonexistent.
          </p>
        </div>

        <!-- Our Solution -->
        <div>
          <h3 class="font-serif text-2xl text-gray-900 mb-4">
            Our solution
          </h3>
          <p class="text-gray-500 leading-relaxed mb-6">
            Censta fractionalizes authenticated collectibles into investable shares through expert curation and securitization technology. Every item in our collection undergoes rigorous authentication by recognized experts, ensuring institutional-grade quality.
          </p>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mt-8">
            <div class="bg-white p-6 rounded-sm border border-gray-200">
              <div class="text-3xl font-serif text-gray-900 mb-2">Expert curation</div>
              <p class="text-gray-500 text-sm leading-relaxed">
                Every collectible is authenticated and curated by recognized experts, providing institutional-grade quality assurance.
              </p>
            </div>
            
            <div class="bg-white p-6 rounded-sm border border-gray-200">
              <div class="text-3xl font-serif text-gray-900 mb-2">Fractional access</div>
              <p class="text-gray-500 text-sm leading-relaxed">
                Invest in high-value collectibles with lower minimums through our fractional ownership model.
              </p>
            </div>
            
            <div class="bg-white p-6 rounded-sm border border-gray-200">
              <div class="text-3xl font-serif text-gray-900 mb-2">Transparent market</div>
              <p class="text-gray-500 text-sm leading-relaxed">
                Our secondary market provides liquidity and transparent pricing, addressing a key concern for wealth managers.
              </p>
            </div>
            
            <div class="bg-white p-6 rounded-sm border border-gray-200">
              <div class="text-3xl font-serif text-gray-900 mb-2">Educational content</div>
              <p class="text-gray-500 text-sm leading-relaxed">
                Access articles and videos about stamps, coins, and collectibles to deepen your expertise.
              </p>
            </div>
          </div>
        </div>

        <!-- Our Approach -->
        <div class="bg-white p-8 rounded-sm border border-gray-200">
          <h3 class="font-serif text-2xl text-gray-900 mb-6">
            How we're building this
          </h3>
          <div class="space-y-6">
            <div class="flex gap-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-black text-white flex items-center justify-center text-sm font-medium">
                1
              </div>
              <div>
                <h4 class="font-medium text-gray-900 mb-2">Starting with HNW collectors</h4>
                <p class="text-gray-500 text-sm leading-relaxed">
                  We're beginning with high-net-worth collectors who understand the value of authenticated assets and can help us refine our curation process.
                </p>
              </div>
            </div>
            
            <div class="flex gap-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-black text-white flex items-center justify-center text-sm font-medium">
                2
              </div>
              <div>
                <h4 class="font-medium text-gray-900 mb-2">Reaching wealth managers</h4>
                <p class="text-gray-500 text-sm leading-relaxed">
                  Through family office conferences and direct outreach, we're connecting with wealth managers who want to offer their clients diversified portfolios.
                </p>
              </div>
            </div>
            
            <div class="flex gap-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-black text-white flex items-center justify-center text-sm font-medium">
                3
              </div>
              <div>
                <h4 class="font-medium text-gray-900 mb-2">Scaling through technology</h4>
                <p class="text-gray-500 text-sm leading-relaxed">
                  Our securitization technology enables fractional ownership at scale, making authenticated collectibles accessible to a broader audience.
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Mission Statement -->
        <div class="text-center py-12">
          <p class="font-serif text-2xl md:text-3xl text-gray-900 leading-relaxed max-w-3xl mx-auto">
            "We believe everyone should have access to authenticated alternative assets that can diversify their portfolio and appreciate over time."
          </p>
          <div class="mt-6 text-sm text-gray-500">
            — Kupa Pounsford & Joshua Rudland-Potter, Co-Founders
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Team Section -->
  <section class="px-6 py-12 bg-[#f5f5f5]">
    <div class="max-w-[1400px] mx-auto relative rounded-sm overflow-hidden bg-[#0a2533] h-[500px] flex flex-col justify-center items-center text-center px-6">
      
      <img 
        src="/generated/image-professional-wealth-managers-and-collect-1765650888310-1.webp" 
        alt="Wealth managers and collectors" 
        class="absolute inset-0 w-full h-full object-cover opacity-30 mix-blend-overlay"
      />
      <div class="absolute inset-0 bg-gradient-to-b from-[#0f3042] to-[#05151e] opacity-90"></div>

      <svg class="absolute inset-0 w-full h-full pointer-events-none" viewBox="0 0 1400 500" fill="none" preserveAspectRatio="none">
        <path d="M-200,400 C100,300 400,50 1600,200" stroke="white" stroke-width="1" stroke-opacity="0.3" vector-effect="non-scaling-stroke" />
        <path d="M-200,400 C200,350 500,150 1600,400" stroke="white" stroke-width="1" stroke-opacity="0.1" vector-effect="non-scaling-stroke" />
      </svg>

      <div class="relative z-10 max-w-2xl">
        <div class="absolute top-[-80px] left-0 flex items-center gap-2 text-white/60 text-[10px] tracking-[0.2em] font-medium uppercase">
          <div class="w-[2px] h-3 bg-white/60"></div>
          Meet the Founders
        </div>

        <h2 class="font-serif text-3xl md:text-5xl text-white mb-6 leading-tight">
          Kupa Pounsford & Joshua Rudland-Potter
        </h2>
        <p class="text-gray-400 text-lg mb-10 leading-relaxed">
          Our founders bring deep expertise in collectibles, finance, and technology to create a platform that serves both collectors and investors.
        </p>
        
        <button class="border border-gray-600 text-white px-6 py-3 rounded text-sm font-medium hover:bg-white hover:text-black transition-colors">
          Get in touch
        </button>
      </div>
    </div>
  </section>

  <Footer />
</div>
