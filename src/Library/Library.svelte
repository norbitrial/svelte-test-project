<script>
    import BookGrid from './BookGrid';
    import Button from '../common/Button';

    const books = [
        {id: 1, title: 'Book 1', author: 'Author 1', cover: '', about: 'random book 1', favorite: true},
        {id: 2, title: 'Book 2', author: 'Author 2', cover: '', about: 'random book 2', favorite: false},
        {id: 3, title: 'Book 3', author: 'Author 3', cover: '', about: 'random book 3', favorite: true},
        {id: 4, title: 'Book 4', author: 'Author 4', cover: '', about: 'random book 4', favorite: false},
    ];

    //export let books;
</script>

<style>

</style>

<header>
    <h1>Hello Library</h1>
</header>

<p>This a library application built with Svelte for fun</p>
<BookGrid books={books} />
<Button>+ Add Book</Button>