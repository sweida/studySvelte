<script>
	import Info from './Info.svelte'

	let pkg = {
		name: 'svelte',
		version: '1.1',
		speed: '2',
		website: 'hello'
	}

	let title = '九歌的博客'
	let count = 0;
	
	$: doubled = count * 2;

	$: if (count >= 10) {
		alert(`count is dangerously high!`);
		count = 9;
	}

	function handleClick() {
		count += 1
	}

	let numbers = [1, 2, 3, 4];

	function addNumber() {
		numbers = [...numbers, numbers.length + 1];
		// numbers.push(numbers.length + 1);
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>


<p>{count} doubled is {doubled}</p>
<button on:click={handleClick}>
	click {count} {count<=1 ? 'time': 'times'} 
</button>
<h1>this is svelte!</h1>
<h1>{title}</h1>

<Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
<Info {...pkg}/>



<style>
	h1 {
		color: purple;
	}
</style>