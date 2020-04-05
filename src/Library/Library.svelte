<script>
    import { onMount } from 'svelte';

    import BookGrid from './BookGrid';
    import Button from '../common/Button';
    import { httpGet } from '../common/api.js';

    let books = [];
    onMount(async function () {
        const { data } = await httpGet('/?_sort=id&_order=desc');
        books = data;
    });
</script>

<style>

</style>

<header>
    <h1>Hello Library</h1>
</header>

<p>This a library application built with Svelte for fun</p>
<BookGrid books={books} />
<Button>+ Add Book</Button>