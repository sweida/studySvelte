<script>
	import Herder from './Header.svelte'
	import Nested from './Nested.svelte'
	import IfElse from './IfElse.svelte'
	import For from './For.svelte'
	import MouseMove from './MouseMove.svelte'
	import Dispa from './Dispa.svelte'


	export let name;

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<IfElse></IfElse>
<For></For>
<MouseMove></MouseMove>
<Dispa></Dispa>

<h1>Hello {name}!</h1>
<p>learn svelte</p>
<Herder></Herder>
<Nested answer={30}></Nested>
<Nested></Nested>


