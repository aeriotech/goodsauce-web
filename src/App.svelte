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
	<!--<div class="container">
		<section class="child">
			<Header />
		</section>
		<section class="child">
			<Filmi />
		</section>
		<section class="child">
			<Linki />
			<Magna />
			<Footer />
		</section>
	</div>-->

	<div class="container">
		<section class="child">
			<Header />
		</section>
		<section class="child">
			<Filmi />
		</section>
		<section class="child">
			<Linki />
			<Magna />
			<Footer />
		</section>
	</div>

	<!--<Header />
	<Filmi />
	<Linki />
	<Magna />
	<Footer />-->
</main>

<style>
	@import url("https://fonts.googleapis.com/css2?family=Secular+One&display=swap");
	@import url("https://fonts.cdnfonts.com/css/mersad");
	@import url("https://fonts.cdnfonts.com/css/pitch-display");
	main {
		width: 100%;
		background: #000000;
		overflow: hidden;
	}
	.container {
		scroll-snap-type: y proximity;
		overflow-y: scroll;
		height: 100vh;
	}
	.child {
		scroll-snap-align: start;
	}

	@media (max-width: 768px) {
		.container {
			scroll-snap-type: none;
			overflow-y: none;
			height: 100vh;
		}
		.child {
			scroll-snap-align: none;
		}
	}
</style>
