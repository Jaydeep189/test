<script>
	import {Router, Route} from 'svelte-navigator'
	import Home from './pages/Home.svelte';
	import Mid from './pages/Mid.svelte';
	import { onMount } from 'svelte';

	let photos = [];
	let photoss = [];
	onMount(async () => {
		const res = await fetch(`https://jsonplaceholder.typicode.com/photos?_limit=5`);
		photos = await res.json();
		const ress = await fetch(`https://jsonplaceholder.typicode.com/comments?postId=1`);
		photoss = await ress.json();
	});
</script>

<main>
	<Router>
		<Route path="/">
			<Home photo= {photos}/>
		</Route>
		<Route path="/mid">
			<Mid comment = {photoss}/>
		</Route>
	</Router>
</main>