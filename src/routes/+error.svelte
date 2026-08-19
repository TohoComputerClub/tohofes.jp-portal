<script>
	import { page } from '$app/stores';
	let currentPath = $derived($page.url.pathname)

</script>

<h1>404 - ページが見つかりません</h1>

{#if $page.status === 404}
	<p>お探しのページは見つかりませんでした。</p>
	<p>以下のリンクをご確認ください：</p>

	<!-- 生成された動的リンク -->
	<a href='https://75th.tohofes.jp{currentPath}'>
		75th.tohofes.jp{currentPath}
	</a>
{:else}
	<p>エラーが発生しました: {$page.status}</p>
{/if}