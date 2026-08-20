<script>
	import { page } from '$app/stores';
	let currentPath = $derived($page.url.pathname);

    export const prerender = true;
</script>

<section class="container mx-auto mt-20">
    <div class="flex flex-col mx-4 md:mx-20">
        <h1 class="text-6xl mx-auto mt-4 md:text-8xl">404</h1>
        <h1 class="text-3xl mx-auto mt-2 md:text-5xl">Not Found</h1>
        <h2 class="text-3xl mx-auto mt-4">ページが見つかりません</h2>
        <hr class="my-10"/>
        {#if $page.status === 404}
            <p class="text-lg mb-4">お探しのページは見つかりませんでした。</p>
            <p class="text-lg">過去の桐朋祭ホームページにアクセスしたい場合は以下のリンクをご確認ください。</p>
            <a href='https://75th.tohofes.jp{currentPath}' class="text-lg w-fit transition-all hover:underline">
                <i class="fa-solid fa-arrow-up-right-from-square mr-1 text-sm"></i>https://75th.tohofes.jp{currentPath}
            </a>
        {:else}
            <p>エラーが発生しました: {$page.status}</p>
        {/if}
        <hr class="my-10"/>
        <a href='/' class="text-lg w-fit transition-all hover:underline">
            <i class="fa-solid fa-house text-sm"></i>トップへ戻る
        </a>
    </div>
</section>