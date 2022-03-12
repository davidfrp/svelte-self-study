<script>
	import Introduction from "./components/Introduction.svelte";
	import Reactivity from "./components/Reactivity.svelte";
	import Props from "./components/Props.svelte";
	import Logic from "./components/Logic.svelte";

	let user = {
		name: 'Heather',
		age: 22,
		avatar: '/images/eye.jpg'
	}

	let posts = [
		{
			author: user,
			message: 'Appreciate where you are. I am in the middle of nowhere. You could be anywhere. The universe is infinite.',
			sentAt: new Date(),
			likes: 5
		},
		{
			author: user,
			message: '',
			sentAt: new Date(),
			likes: 3
		}
	]
</script>

<main>
	<Introduction />
	<Reactivity />
	<Props {...user} />
	<Logic {posts} />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>