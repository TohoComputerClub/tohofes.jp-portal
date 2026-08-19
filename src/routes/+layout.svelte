<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="stylesheet" href="https://cdn.atserver186.jp/libs/fontawesome/css/all.min.css" />
	<link rel="icon" href={favicon} />
</svelte:head>

<header class="fixed items-center top-4 left-1/2 z-20 w-[90%] -translate-x-1/2 rounded-4xl border border-black/10 bg-white/80 backdrop-blur-md transition-all duration-500 md:w-[80%] lg:w-[60%]">
	<div class="flex p-2">
		<a href="/" class="flex transition h-12">
			<p class="m-auto ml-2 hidden md:block">桐朋祭</p>
		</a>
		<nav class="ml-auto flex list-none items-center gap-5 whitespace-nowrap transition">
			<li><a href="/" class="ml-1 text-sm tracking-wider transition">Home</a></li>
			<li>
				<a href="/about" class="ml-3 text-sm tracking-wider transition">About</a>
			</li>
			<li>
				<a href="/blog" class="ml-3 text-sm tracking-wider transition">Blog</a>
			</li>
			<li>
				<a href="/" class="ml-3 text-sm tracking-wider transition" target="_blank"
					>Docs<i class="fa-solid fa-arrow-up-right-from-square ml-1"></i></a
				>
			</li>
		</nav>
	</div>
</header>

{@render children()}
