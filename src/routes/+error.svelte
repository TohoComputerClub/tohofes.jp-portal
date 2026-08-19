<script>
	import { page } from '$app/stores';
	let currentPath = $derived($page.url.pathname)

</script>

<section class="container mx-auto mt-20">
    <div class="flex flex-col mx-4 md:mx-20">
        <h1 class="text-8xl mx-auto mt-4">404</h1>
        <h1 class="text-5xl mx-auto mt-2">Not Found</h1>
        <h2 class="text-3xl mx-auto mt-4">ページが見つかりません</h2>
        <hr class="my-10"/>
        {#if $page.status === 404}
            <p>お探しのページは見つかりませんでした。</p>
            <p>過去の桐朋祭ホームページにアクセスしたい場合は以下のリンクをご確認ください。</p>
            <a href='https://75th.tohofes.jp{currentPath}'>
                https://75th.tohofes.jp{currentPath}
            </a>
        {:else}
            <p>エラーが発生しました: {$page.status}</p>
        {/if}
    </div>
</section>