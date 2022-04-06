<script lang="ts">
  import {chainTempo} from '$lib/blockchain/chainTempo';
  import {wallet} from '$lib/blockchain/wallet';

  import {context} from '$lib/plugin/plugin';
  
  chainTempo.startOrUpdateProvider(wallet.provider);
</script>

{#if $context.initialized}
    <p class="text-lg font-bold">GM</p>
    <p>I hope you're having a great day :)</p>
    <p>More plugins to come!</p>
    <p class="p-2">- fraserd.eth</p>
{:else}
  <p>Waiting for initialization to complete....</p>
{/if}
