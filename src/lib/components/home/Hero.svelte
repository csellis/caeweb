<script lang="ts">
  import { fade } from 'svelte/transition';
</script>

<section class="relative h-screen flex items-center justify-center bg-gradient-to-br from-primary to-primary-light text-white">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center" in:fade={{ duration: 1000 }}>
      <h1 class="text-4xl sm:text-6xl font-heading font-bold mb-6">
        Transforming Business Through Technology
      </h1>
      <p class="text-xl sm:text-2xl mb-8 max-w-2xl mx-auto">
        We create innovative software solutions that drive efficiency and growth for SMEs.
      </p>
      <a
        href="/contact"
        class="inline-block bg-white text-primary px-8 py-3 rounded-full font-semibold hover:bg-gray-100 transition-colors"
      >
        Book a Consultation
      </a>
    </div>
  </div>
</section>