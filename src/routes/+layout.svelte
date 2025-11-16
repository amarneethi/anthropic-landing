<!-- +layout.svelte -->
<script>
	import favicon from '$lib/assets/favicon.svg';
	import '../app.css';
	let mediaAll = $state(false);

	let { children } = $props();
</script>

<svelte:head>
	<title>Home \ Anthropic</title>
	<meta
		content="Anthropic is an AI safety and research company that's working to build reliable, interpretable, and steerable AI systems."
		name="description"
	/>
	<meta
		name="description"
		content="Turn your designs into functional interfaces, demos and production grade code in minutes, not weeks."
	/>
	<link rel="icon" href={favicon} />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Ephesis&family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap"
		rel="stylesheet"
		media={mediaAll ? 'all' : 'print'}
		onload={() => {
			mediaAll = true;
		}}
	/>
</svelte:head>

{@render children()}
