<script lang="ts">
  import { writable } from 'svelte/store';

  export const mode = writable<'normal' | 'trading'>('normal');

  let currentMode = 'normal';

  function toggleMode() {
    currentMode = currentMode === 'normal' ? 'trading' : 'normal';
    mode.set(currentMode);
  }
</script>

<button
  on:click={toggleMode}
  class="flex items-center gap-2 px-3 py-1.5 rounded-xl border border-border text-foreground bg-muted hover:bg-accent transition-colors text-sm"
>
  {#if currentMode === 'normal'}
    <span class="text-lg">🧠</span>
    <span>KI-Modus</span>
  {:else}
    <span class="text-lg">📊</span>
    <span>Trading-Modus</span>
  {/if}
</button>
