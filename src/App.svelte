<script lang="ts">
  // import svelteLogo from './assets/svelte.svg';
  // import viteLogo from '/vite.svg';
  // import Counter from './lib/Counter.svelte';
  import './app.css';
  import { ModeWatcher, toggleMode } from 'mode-watcher';
  import { Button } from '$lib/components/ui/button';
  import SunIcon from "@lucide/svelte/icons/sun";
  import MoonIcon from "@lucide/svelte/icons/moon";
</script>

<main>
  <h1 class="text-3xl font-bold underline">
Vite + Svelte</h1>

<Button onclick={toggleMode} variant="outline" size="icon">
  <SunIcon
    class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 !transition-all dark:-rotate-90 dark:scale-0"
  />
  <MoonIcon
    class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 !transition-all dark:rotate-0 dark:scale-100"
  />
  <span class="sr-only">Toggle theme</span>
</Button>
<ModeWatcher />
</main>
