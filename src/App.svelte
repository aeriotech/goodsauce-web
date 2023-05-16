<script>
	import Header from "./components/headernew.svelte";
	import Filmi from "./components/filmi.svelte";
	import Linki from "./components/linki.svelte";
	import Magna from "./components/magnadogs.svelte";
	import Footer from "./components/footer.svelte";
	import { onMount } from "svelte";
	/*
	let loading = true;
	
	onMount(() => {
		document.onload = () => {
			loading = false;
		};
	});
	*/
</script>

<main>
	<Header />
	<Filmi />
	<Linki />
	<Magna />
	<Footer />
</main>

<style>
	main {
		width: 100%;
		background: #000000;
		overflow: hidden;
	}
	@import url("https://fonts.googleapis.com/css2?family=Secular+One&display=swap");
	@import url('https://fonts.cdnfonts.com/css/mersad');
	@import url('https://fonts.cdnfonts.com/css/pitch-display');
</style>
