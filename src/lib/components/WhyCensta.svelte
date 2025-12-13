<script>
  import SectionLabel from './SectionLabel.svelte';
</script>

<section class="bg-[#f5f5f5] px-6 py-24">
  <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-12 gap-12">
    <div class="lg:col-span-3">
      <SectionLabel label="Why Censta" />
    </div>
    
    <div class="lg:col-span-9 grid grid-cols-1 md:grid-cols-2 gap-16">
      <div>
        <h2 class="font-serif text-3xl md:text-4xl leading-tight text-gray-900 mb-6">
          Censta democratizes access to authenticated alternative assets through expert curation
        </h2>
        <p class="text-gray-500 leading-relaxed">
          Every collectible is expertly authenticated and curated, giving affluent millennials and collectors access to a $370B market previously reserved for high-net-worth individuals.
        </p>
      </div>
      
      <div class="flex gap-12 items-end pb-2">
        <div class="flex flex-col gap-1">
            <span class="text-4xl font-serif text-gray-900 mb-1">$370B</span>
            <span class="text-xs text-gray-400">alternative assets market</span>
        </div>
        <div class="flex flex-col gap-1">
            <span class="text-4xl font-serif text-gray-900 mb-1">100%</span>
            <span class="text-xs text-gray-400">authenticated collectibles</span>
        </div>
      </div>
    </div>
  </div>
</section>
