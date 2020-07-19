<script>
	import Helper from './components/Helper.svelte';
</script>

<main class="main">
	<textarea class="main__textarea main__textarea--field" autofocus></textarea>
	<div class="main__textarea main__textarea--preview"></div>

	<Helper />
</main>

<style>
.main {
	display: grid;
	grid-template-columns: repeat(2, 1fr);
}

.main__textarea {
	padding: 40px;
	font-size: 16px;
	height: 100vh;
}

.main__textarea--field {
	font-family: inherit;
	border: 0;
	outline: 0;
	resize: none;
}

.main__textarea--preview {
	background-color: #eaeaea;
}
</style>