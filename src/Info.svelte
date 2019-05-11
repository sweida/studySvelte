<script>
	export let name;
	export let version;
	export let speed;
	export let website;

	function handleClick() {
		alert('no more alerts')
	}
</script>

<button on:click|once={handleClick}>
	noly one alert
</button>


<p>
	The <code>{name}</code> package is {speed} fast.
	Download version {version} from <a href="https://www.npmjs.com/package/{name}">npm</a>
	and <a href={website}>learn more here</a>
</p>