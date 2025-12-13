<script lang="ts">
  import { slide } from 'svelte/transition';
  
  interface FAQItem {
    question: string;
    answer: string;
  }

  const faqs: FAQItem[] = [
    { question: "How does fractional ownership work?", answer: "Censta uses securitization technology to divide authenticated collectibles into investable shares. Each share represents partial ownership of a verified asset, allowing you to invest in high-value collectibles without purchasing the entire item." },
    { question: "Are all collectibles authenticated?", answer: "Yes, every collectible on Censta is expertly authenticated and curated by specialists. We work with leading authentication services to ensure 100% authenticity of stamps, coins, and other alternative assets on our platform." },
    { question: "Who can invest with Censta?", answer: "Censta is designed for affluent millennials seeking portfolio diversification and high-net-worth collectors. We work with wealth managers and family offices to provide access to authenticated alternative assets." },
    { question: "What is the secondary market?", answer: "Censta provides transparent secondary market access, allowing you to buy and sell fractional shares of collectibles. This addresses traditional liquidity concerns with alternative assets and gives you flexibility in managing your portfolio." },
    { question: "What types of collectibles are available?", answer: "We currently offer authenticated stamps, coins, and other rare collectibles. Each asset is selected through our expert curation process, focusing on items with strong historical significance and investment potential." },
    { question: "How do I get started?", answer: "Simply create an account, browse our curated collection of authenticated collectibles, and start investing in fractional shares. Our platform guides you through the process of diversifying your portfolio with alternative assets." },
    { question: "What makes Censta different from other platforms?", answer: "Censta combines expert curation, full authentication, securitization technology, and transparent secondary markets. We focus specifically on the $370B alternative assets market, bringing institutional-grade collectibles investing to individual investors." }
  ];

  let openIndex: number | null = null;

  function toggle(index: number) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<section class="bg-[#f5f5f5] px-6 py-24">
  <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-12 gap-12">
    <div class="lg:col-span-4">
      <h2 class="font-serif text-4xl text-gray-900 mb-6">
        Frequently asked questions
      </h2>
      <a href="/" class="text-sm text-gray-900 border-b border-gray-300 pb-0.5 hover:border-black transition-colors">See all support</a>
    </div>
    
    <div class="lg:col-span-8">
      <div class="border-t border-gray-200">
        {#each faqs as faq, i}
          <div class="border-b border-gray-200">
            <button 
              class="w-full py-6 flex justify-between items-center text-left hover:bg-gray-50 transition-colors"
              on:click={() => toggle(i)}
            >
              <span class="text-lg text-gray-800">{faq.question}</span>
              <span class="text-2xl font-light text-gray-400 ml-4">
                {openIndex === i ? '−' : '+'}
              </span>
            </button>
            {#if openIndex === i}
              <div transition:slide class="pb-6 text-gray-500 leading-relaxed">
                {faq.answer}
              </div>
            {/if}
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
