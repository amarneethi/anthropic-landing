<script>
	import { slide } from 'svelte/transition';
	const announcementItemClasses =
		'flex cursor-pointer items-center justify-between border-b border-anthropic-darkbrown py-8'; let showMenu = $state(false);
</script>

{#snippet arrowRight()}
	<svg
		xmlns="http://www.w3.org/2000/svg"
		width="32"
		height="32"
		viewBox="0 0 24 24"
		fill="none"
		stroke="currentColor"
		stroke-width="2"
		stroke-linecap="round"
		stroke-linejoin="round"
		class="lucide lucide-arrow-right"
	>
		<path d="M5 12h14" />
		<path d="m12 5 7 7-7 7" />
	</svg>
{/snippet}
<header class="sticky top-0 z-50 bg-anthropic-beige">
	<div class="max-w-9xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex items-center justify-between py-4">
			<div class="text-2xl font-bold">A\</div>
			<nav class="text-md hidden items-center justify-end space-x-8 md:flex">
				<a href="#" class=" hover:text-gray-600">Research</a>
				<a href="#" class=" hover:text-gray-600">Economic Futures</a>
				<a href="#" class=" hover:text-gray-600">Commitments</a>
				<a href="#" class=" hover:text-gray-600">Learn</a>
				<a href="#" class=" hover:text-gray-600">News</a>
				<button class="text-md rounded-xl bg-black px-8 py-3 text-white hover:bg-gray-800">
					Try Claude
				</button>
			</nav>
			<button
				class="md:hidden"
				onclick={() => {
					console.log('clicked');
					showMenu = !showMenu;
				}}
			>
				<svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M4 6h16M4 12h16M4 18h16"
					></path>
				</svg>
			</button>
		</div>
		<!-- Mobile menu -->
		{#if showMenu}
			<nav transition:slide class="flex flex-col space-y-4 pb-4 md:hidden">
				<a href="#" class="hover:text-gray-600">Research</a>
				<a href="#" class="hover:text-gray-600">Economic Futures</a>
				<a href="#" class="hover:text-gray-600">Commitments</a>
				<a href="#" class="hover:text-gray-600">Learn</a>
				<a href="#" class="hover:text-gray-600">News</a>
				<button class="text-md rounded-xl bg-black px-8 py-3 text-white hover:bg-gray-800">
					Try Claude
				</button>
			</nav>
		{/if}
	</div>
</header>

<!-- Hero Section -->
<section class="max-w-8xl mx-4 px-4 py-12 sm:px-6 md:mx-24 md:py-24 lg:px-2">
	<div class="flex flex-col-reverse items-center gap-4 md:flex-row">
		<div>
			<h1 class="font-montserrat text-4xl leading-tight font-bold md:text-5xl lg:text-6xl">
				AI <span class="underline decoration-4">research</span> and
				<span class="underline decoration-4">products</span> that put safety at the frontier
			</h1>
			<p class="font-serif text-lg leading-relaxed text-gray-700 md:text-xl">
				AI will have a vast impact on the world. Anthropic is a public benefit corporation dedicated
				to securing its benefits and mitigating its risks.
			</p>
		</div>
		<div class="flex justify-center lg:justify-end">
			<!-- Placeholder for hand with data tree illustration -->
			<img
				src="/handIllustration.svg"
				alt="Hand holding a data tree illustration"
				class="w-80 md:w-md"
			/>
		</div>
	</div>
</section>

<!-- Claude Sonnet Section -->
<section class="max-w-8xl mx-4 px-4 py-12 sm:px-6 md:mx-24 md:py-12 lg:px-2">
	<div class="rounded-3xl bg-anthropic-brown p-8 md:p-12">
		<div class="grid grid-cols-1 gap-8 lg:grid-cols-2">
			<div>
				<h2 class="mb-4 text-3xl font-semibold md:text-5xl">Claude Sonnet 4.5</h2>
				<p class="mb-8 font-serif text-2xl text-gray-700">
					Introducing the best model in the world for agents, coding, and computer use.
				</p>
				<button class="rounded-md bg-black px-6 py-3 text-sm text-white hover:bg-gray-800">
					Read announcement
				</button>
			</div>
			<div>
				<p class="text-md font-bold text-gray-600">Learn more</p>
				<div class={announcementItemClasses}>
					<div>
						<p class="text-2xl text-gray-900 opacity-75">Introducing Claude Haiku 4.5</p>
					</div>
					{@render arrowRight()}
				</div>
				<div class={announcementItemClasses}>
					<p class="text-2xl text-gray-900 opacity-75">
						Managing context on the Claude Developer Platform
					</p>
					{@render arrowRight()}
				</div>
				<div class={announcementItemClasses}>
					<p class="text-2xl text-gray-900 opacity-75">Model details</p>
					{@render arrowRight()}
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Reading the Mind Section -->
<section class="max-w-9xl mx-auto border-b px-4 py-12 sm:px-6 md:mx-24 md:mt-12 md:py-16 lg:px-8">
	<div class="grid grid-cols-1 items-center gap-8 lg:grid-cols-3">
		<div class="lg:col-span-2">
			<div
				class="relative flex items-center justify-center overflow-hidden rounded-3xl bg-anthropic-brown"
			>
				<img
					src="/readingthemindofanai.webp"
					alt="Reading the mind of an AI"
					class="h-full w-full"
				/>

				<button
					class="absolute z-10 flex h-16 w-16 items-center justify-center rounded-full bg-white shadow-lg transition-transform hover:scale-110"
				>
					<svg class="ml-1 h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
						<path d="M8 5v14l11-7z" />
					</svg>
				</button>
			</div>
		</div>
		<div class="rounded-2xl p-8">
			<p class="absolute font-ephesis text-9xl">"</p>
			<p class="mt-16 font-serif text-2xl leading-relaxed">
				When you're talking to a large language model, what exactly is it that you're talking to?
			</p>
		</div>
	</div>
</section>

<!-- Mission Statement -->
<section class="max-w-8xl mx-auto px-4 py-12 sm:px-6 md:mx-24 md:py-16 lg:px-8">
	<div class="grid grid-cols-1 gap-12 lg:grid-cols-3">
		<div class="lg:col-span-1">
			<h2 class="mb-6 text-3xl font-bold md:text-4xl">
				At Anthropic, we build AI to serve humanity's long-term well-being.
			</h2>
		</div>
		<div class="font-serif lg:col-span-2">
			<p class="mb-6 text-lg leading-relaxed text-gray-700">
				While no one can foresee every outcome AI will have on society, we do know that designing
				powerful technologies requires both bold steps forward and intentional pauses to consider
				the effects.
			</p>
			<p class="text-lg leading-relaxed text-gray-700">
				That's why we focus on building tools with human benefit at their foundation, like Claude.
				Through our daily research, policy work, and product design, we aim to show what responsible
				AI development looks like in practice.
			</p>
		</div>
	</div>
</section>

<!-- Three Cards Section -->
<section class="max-w-8xl mx-auto px-4 py-12 sm:px-6 md:mx-24 md:py-16 lg:px-8">
	<div class="grid grid-cols-1 gap-10 md:grid-cols-3">
		<!-- Card 1 -->
		<div class="space-y-4 rounded-3xl bg-[#E8DED3] p-8">
			<img
				class="mx-auto w-48"
				src="/Hands-Build.svg"
				alt="Hands building carefully with safety in mind"
			/>
			<h3 class="font-montserrat text-xl font-semibold">Core Views on AI Safety</h3>
		</div>
		<!-- Card 2 -->
		<div class="space-y-4 rounded-3xl bg-anthropic-sage p-8">
			<img class="mx-auto w-48" src="/Hands-Stack.svg" alt="Hands stacking blocks carefully" />
			<h3 class="font-montserrat text-xl font-semibold">Anthropic's Responsible Scaling Policy</h3>
		</div>
		<!-- Card 3 -->
		<div class="space-y-4 rounded-3xl bg-anthropic-lavender p-8">
			<img class="mx-auto w-48" src="/Objects-Puzzle.svg" alt="Puzzle pieces coming together" />
			<h3 class="font-montserrat text-xl font-semibold">
				Anthropic Academy: Learn to build with Claude
			</h3>
		</div>
	</div>
</section>

<!-- Featured Section -->
<section
	class="max-w-8xl mx-auto grid grid-cols-1 px-4 py-12 sm:px-6 md:mx-24 md:py-16 lg:grid-cols-3 lg:px-8"
>
	<h2 class="mb-8 text-2xl font-bold lg:col-span-1">Featured</h2>
	<div class="space-y-4 lg:col-span-2">
		<div
			class="grid cursor-pointer grid-cols-1 gap-4 border-b border-gray-300 py-4 transition-colors hover:bg-white/50 md:grid-cols-5"
		>
			<div class="font-semibold md:col-span-3">Introducing Haiku 4.5</div>
			<div class="text-gray-600">Announcements</div>
			<div class="text-right text-gray-600">Oct 16, 2025</div>
		</div>
		<div
			class="grid cursor-pointer grid-cols-1 gap-4 border-b border-gray-300 py-4 transition-colors hover:bg-white/50 md:grid-cols-5"
		>
			<div class="font-semibold md:col-span-3">Introducing Sonnet 4.5</div>
			<div class="text-gray-600">Announcements</div>
			<div class="text-right text-gray-600">Sep 24, 2025</div>
		</div>
		<div
			class="grid cursor-pointer grid-cols-1 gap-4 border-b border-gray-300 py-4 transition-colors hover:bg-white/50 md:grid-cols-5"
		>
			<div class="font-semibold md:col-span-3">Anthropic Economic Index</div>
			<div class="text-gray-600">Economic Research</div>
			<div class="text-right text-gray-600">Sep 19, 2025</div>
		</div>
		<div
			class="grid cursor-pointer grid-cols-1 gap-4 border-b border-gray-300 py-4 transition-colors hover:bg-white/50 md:grid-cols-5"
		>
			<div class="font-semibold md:col-span-3">Claude Opus 4.1</div>
			<div class="text-gray-600">Announcements</div>
			<div class="text-right text-gray-600">Aug 05, 2025</div>
		</div>
		<div
			class="grid cursor-pointer grid-cols-1 gap-4 border-b border-gray-300 py-4 transition-colors hover:bg-white/50 md:grid-cols-5"
		>
			<div class="font-semibold md:col-span-3">Project Verd</div>
			<div class="text-gray-600">Policy</div>
			<div class="text-right text-gray-600">Jun 25, 2025</div>
		</div>
		<div
			class="grid cursor-pointer grid-cols-1 gap-4 border-b border-gray-300 py-4 transition-colors hover:bg-white/50 md:grid-cols-5"
		>
			<div class="font-semibold md:col-span-3">Agentic Management</div>
			<div class="text-gray-600">Alignment</div>
			<div class="text-right text-gray-600">Jun 20, 2025</div>
		</div>
		<div
			class="grid cursor-pointer grid-cols-1 gap-4 border-b border-gray-300 py-4 transition-colors hover:bg-white/50 md:grid-cols-5"
		>
			<div class="font-semibold md:col-span-3">Tracing the thoughts of a large language model</div>
			<div class="text-gray-600">Interpretability</div>
			<div class="text-right text-gray-600">Mar 27, 2025</div>
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="mx-auto max-w-7xl px-4 py-16 sm:px-6 md:py-24 lg:px-8">
	<div class="text-center">
		<h2 class="mx-auto mb-8 max-w-xl font-montserrat text-6xl font-semibold md:text-6xl">
			Want to help us build the future of safe AI?
		</h2>
		<div class="flex flex-col justify-center gap-4 sm:flex-row">
			<button class="rounded-md bg-black px-8 py-3 text-sm text-white hover:bg-gray-800">
				See open roles
			</button>
			<button
				class="rounded-md border-2 border-black px-8 py-3 text-sm text-black transition-colors hover:bg-black hover:text-white"
			>
				Speak with sales
			</button>
		</div>
	</div>
</section>

<!-- Footer -->
<footer class="bg-black text-white">
	<div class="mx-auto max-w-7xl px-4 py-12 sm:px-6 lg:px-8">
		<div class="mb-8 grid grid-cols-2 gap-8 md:grid-cols-4">
			<!-- Products -->
			<div>
				<h3 class="my-4 mt-8 font-bold">Products</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">Claude</a></li>
					<li><a href="#" class="hover:text-white">Claude Code</a></li>
					<li><a href="#" class="hover:text-white">iOS and Android</a></li>
					<li><a href="#" class="hover:text-white">Claude in Excel</a></li>
					<li><a href="#" class="hover:text-white">Team plan</a></li>
					<li><a href="#" class="hover:text-white">Enterprise plan</a></li>
					<li><a href="#" class="hover:text-white">Download apps</a></li>
					<li><a href="#" class="hover:text-white">Log in to Claude</a></li>
				</ul>
				<h3 class="my-4 mt-8 font-bold">Models</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">Opus</a></li>
					<li><a href="#" class="hover:text-white">Sonnet</a></li>
					<li><a href="#" class="hover:text-white">Haiku</a></li>
				</ul>
			</div>

			<!-- Solutions -->
			<div>
				<h3 class="my-4 mt-8 font-bold">Solutions</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">AI agents</a></li>
					<li><a href="#" class="hover:text-white">Code modernization</a></li>
					<li><a href="#" class="hover:text-white">Coding</a></li>
					<li><a href="#" class="hover:text-white">Customer support</a></li>
					<li><a href="#" class="hover:text-white">Education</a></li>
					<li><a href="#" class="hover:text-white">Financial services</a></li>
					<li><a href="#" class="hover:text-white">Government</a></li>
					<li><a href="#" class="hover:text-white">Life sciences</a></li>
				</ul>

				<h3 class="my-4 mt-8 font-bold">Claude Developer Platform</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">Overview</a></li>
					<li><a href="#" class="hover:text-white">Developer docs</a></li>
					<li><a href="#" class="hover:text-white">Pricing</a></li>
					<li><a href="#" class="hover:text-white">Amazon Bedrock</a></li>
					<li><a href="#" class="hover:text-white">Google Cloud’s Vertex AI</a></li>
					<li><a href="#" class="hover:text-white">Console login</a></li>
				</ul>
			</div>

			<!-- Learn -->
			<div>
				<h3 class="my-4 mt-8 font-bold">Learn</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">Blog</a></li>
					<li><a href="#" class="hover:text-white">Courses</a></li>
					<li><a href="#" class="hover:text-white">Use cases</a></li>
					<li><a href="#" class="hover:text-white">Connectors</a></li>
					<li><a href="#" class="hover:text-white">Customer stories</a></li>
					<li><a href="#" class="hover:text-white">Engineering at Anthropic</a></li>
					<li><a href="#" class="hover:text-white">Events</a></li>
					<li><a href="#" class="hover:text-white">Powered by Claude</a></li>
				</ul>
				<h3 class="my-4 mt-8 font-bold">Resources</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">API status</a></li>
					<li><a href="#" class="hover:text-white">Help center</a></li>
					<li><a href="#" class="hover:text-white">Documentation</a></li>
					<li><a href="#" class="hover:text-white">Community</a></li>
				</ul>
			</div>

			<!-- Company -->
			<div>
				<h3 class="my-4 mt-8 font-bold">Help and security</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">Availability</a></li>
					<li><a href="#" class="hover:text-white">Status</a></li>
					<li><a href="#" class="hover:text-white">Support center</a></li>
				</ul>

				<h3 class="my-4 mt-8 font-bold">Terms and policies</h3>
				<ul class="space-y-2 text-sm text-anthropic-brown">
					<li><a href="#" class="hover:text-white">Privacy choices</a></li>
					<li><a href="#" class="hover:text-white">Privacy policy</a></li>
					<li><a href="#" class="hover:text-white">Terms of service: Commercial</a></li>
					<li><a href="#" class="hover:text-white">Terms of service: Consumer</a></li>
					<li><a href="#" class="hover:text-white">Usage Policy</a></li>
				</ul>
			</div>
		</div>

		<div class="border-t border-gray-800 pt-8">
			<div class="flex flex-col items-center justify-between md:flex-row">
				<div class="mb-4 text-2xl font-bold md:mb-0">A\</div>
				<div class="mb-4 text-sm text-gray-400 md:mb-0">© 2025 Anthropic PBC</div>
				<div class="flex space-x-4">
					<a href="#" class="text-gray-400 hover:text-white">
						<svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24"
							><path
								d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"
							></path></svg
						>
					</a>
					<a href="#" class="text-gray-400 hover:text-white">
						<svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24"
							><path
								d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"
							></path><circle cx="4" cy="4" r="2"></circle></svg
						>
					</a>
					<a href="#" class="text-gray-400 hover:text-white">
						<svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24"
							><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
							></path><polyline points="22,6 12,13 2,6" fill="none" stroke="black" stroke-width="2"
							></polyline></svg
						>
					</a>
				</div>
			</div>
		</div>
	</div>
</footer>
