<script lang="ts">
  export let theme: 'light' | 'dark';
  export let toggleTheme: () => void;

  let isMenuOpen = false;
  const navigation = [
    { name: 'Home', href: '/' },
    { name: 'Services', href: '/services' },
    { name: 'About', href: '/about' },
    { name: 'Blog', href: '/blog' },
    { name: 'Contact', href: '/contact' },
  ];
</script>

<header class="fixed w-full bg-white dark:bg-gray-900 shadow-sm z-50">
  <nav class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between h-16">
      <div class="flex">
        <a href="/" class="flex items-center">
          <span class="text-xl font-heading font-bold text-primary dark:text-white">CAE Webdevelopment</span>
        </a>
      </div>

      <!-- Desktop Navigation -->
      <div class="hidden sm:flex sm:items-center sm:space-x-8">
        {#each navigation as item}
          <a
            href={item.href}
            class="text-gray-700 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors"
          >
            {item.name}
          </a>
        {/each}
        
        <button
          on:click={toggleTheme}
          class="p-2 rounded-full hover:bg-gray-100 dark:hover:bg-gray-800 transition-colors"
          aria-label="Toggle theme"
        >
          {#if theme === 'light'}
            <!-- Moon icon -->
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" />
            </svg>
          {:else}
            <!-- Sun icon -->
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
            </svg>
          {/if}
        </button>
      </div>

      <!-- Mobile menu button -->
      <div class="flex items-center sm:hidden">
        <button
          on:click={() => isMenuOpen = !isMenuOpen}
          class="inline-flex items-center justify-center p-2 rounded-md text-gray-700 dark:text-gray-300"
        >
          <svg
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            {#if isMenuOpen}
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            {:else}
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            {/if}
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile Navigation -->
    {#if isMenuOpen}
      <div class="sm:hidden">
        <div class="pt-2 pb-3 space-y-1">
          {#each navigation as item}
            <a
              href={item.href}
              class="block px-3 py-2 text-base font-medium text-gray-700 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors"
            >
              {item.name}
            </a>
          {/each}
        </div>
      </div>
    {/if}
  </nav>
</header>