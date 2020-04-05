<script>
    import BookCover from './BookCover';
    import Heart from './Heart';
    export let books = [];

    console.log(books);
</script>

<style>
    li {
        display: inline;
        list-style: none;
    }

    .grid-header {
        background-color: lightgray;
    }

    .grid-line {
        text-decoration: darkblue;
    }
</style>

<div>Books [{books.length}]:</div>
<ul class="grid-header">
    <li>Favorite</li>
    <li>Id</li>
    <li>Title</li>
    <li>About</li>
</ul>
{#each books as book}
    <ul class="grid-line">
        <li>
            {#if book.favorite}
                <Heart />
            {/if}
        </li>
        <li>{book.id}</li>
        <li><BookCover book={book} /></li>
        <li>{book.about}</li>
    </ul>
{/each}