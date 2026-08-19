<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<header class="fixed top-4 left-1/2 z-20 w-[90%] -translate-x-1/2 rounded-4xl border border-black/10 bg-white/80 backdrop-blur-md transition-all duration-500 md:w-[80%] lg:w-[60%]">
	<div class="flex">
		<a href="/">
			<p>tohofes.jp</p>
		</a>
		<nav class="ml-auto flex list-none items-center gap-5 whitespace-nowrap transition">
			<li><a href="/" class="ml-1 text-sm tracking-wider transition">Home</a></li>
			<li>
				<a href="/about" class="ml-3 text-sm tracking-wider transition">About</a>
			</li>
		</nav>
	</div>
</header>

{@render children()}
