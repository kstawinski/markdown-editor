<script>
	import Helper from './components/Helper.svelte';
	import marked from 'marked';

	let text = '# Hello world!';
</script>

<main class="main">
	<textarea class="main__textarea main__textarea--field" autofocus bind:value={text}></textarea>
	<div class="main__textarea main__textarea--preview markdown-body">{@html marked(text)}</div>

	<Helper />
</main>

<style>
.main {
	display: grid;
	grid-template-columns: repeat(2, 1fr);
}

.main__textarea {
	padding: 40px;
	height: 100vh;
}

.main__textarea--field {
	font-size: 16px;
	font-family: inherit;
	border: 0;
	outline: 0;
	resize: none;
}

.main__textarea--preview {
	background-color: #f7f7f7;
}
</style>