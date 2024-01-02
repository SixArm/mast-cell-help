<script lang="ts">
	let menuButtonIsOpen = false;
	import MenuButton from './MenuButton.svelte';
	import MenuContent from './MenuContent.svelte';
</script>

<style lang="postcss">
nav a {
    @apply text-black no-underline;
}
</style>

<header class="mb-8 border-b-2">
    <nav class="m-4">
        <div class="flex items-center">
            <MenuButton bind:isOpen={menuButtonIsOpen} />
            <div class="flex-1 text-left">
                <a class="font-bold" href="https://mastcell.help">MastCell.Help Home</a>
            </div>
        </div>
        <MenuContent bind:isOpen={menuButtonIsOpen} />
    </nav>

</header>
