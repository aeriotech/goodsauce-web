<script>
	import Header from "./components/headernew.svelte";
	import Filmi from "./components/filmi.svelte";
	import Linki from "./components/linki.svelte";
	import Magna from "./components/magnadogs.svelte";
	import Footer from "./components/footer.svelte";
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
</style>
