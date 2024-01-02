<script lang="ts">
    export let isOpen = false;
    import Open from '$lib/MenuButtonOpen.svelte';
    import Shut from '$lib/MenuButtonShut.svelte';
</script>

<button id="MenuButton" type="button" on:click={() => (isOpen = !isOpen)} class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white" aria-controls="mobile-menu" aria-expanded="false">
    <span class="absolute -inset-0.5"></span>
    <span class="sr-only">Open main menu</span>
    {#if isOpen}
        <Open />
    {:else}    
        <Shut />
    {/if}
</button>
