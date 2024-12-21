<script lang="ts">
  import '@fontsource/outfit';
  import '@fontsource/inter';
  import '../app.css';
  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';

  let theme: 'light' | 'dark' = 'light';

  function toggleTheme() {
    theme = theme === 'light' ? 'dark' : 'light';
    document.documentElement.classList.toggle('dark', theme === 'dark');
  }
</script>

<div class="min-h-screen bg-background text-foreground">
  <Header {theme} {toggleTheme} />
  <slot />
  <Footer />
</div>