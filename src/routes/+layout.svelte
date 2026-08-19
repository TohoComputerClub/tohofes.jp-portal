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
			<!--s: souce-c-link-pc-->
			<li class="hidden md:flex">
				<span>|</span>
			</li>
			<li class="hidden md:flex">
				<a
					href="https://github.com/TohoComputerClub/tohofes.jp-portal/"
					class="text-sm tracking-wider transition"
					target="_blank"
					title="Github"><i class="fa-brands fa-github"></i></a
				>
			</li>
			<li class="hidden md:flex">
				<a
					href="https://gitlab.atserver186.jp/t-aoki186/tohofes.jp-portal/"
					class="mr-4 text-sm tracking-wider transition"
					target="_blank"
					title="Gitlab"><i class="fa-brands fa-gitlab"></i></a
				>
			</li>
			<!--e: souce-c-link-pc-->
			<!---->
			<!--s: souce-c-link-sp-->
			<li class="flex md:hidden">
				<a href="/sauce" class="mr-4 text-xs tracking-wider transition" title="Souce"
					><i class="fa-solid fa-code"></i></a
				>
			</li>
			<!--e: souce-c-link-sp-->
		</nav>
	</div>
</header>

<main class="min-h-screen">
	{@render children()}
</main>

<footer class="bg-black py-8">
	<div class="container mx-auto flex">
		<p class="text-white">&copy; 2026 TohoFes. | tohofes.jp All Rights Reserved. 本サイトの無断転載は、固くこれを禁じます。</p>
	</div>
</footer>
