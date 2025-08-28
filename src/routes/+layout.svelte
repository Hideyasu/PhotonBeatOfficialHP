<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="min-h-screen flex flex-col">
<!--  // headerを書く -->
    <main class="flex-1">
        {@render children?.()}
    </main>
        <!-- // footerを書く -->
</div>
