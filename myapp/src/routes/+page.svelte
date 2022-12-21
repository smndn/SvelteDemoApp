<h1>Welcome to Simon's Demo Svelte App</h1>

<script>
	let count = 0;
	$: doubled = count * 2;
    $: tripled = count * 3;
    $: console.log('the count is ' + count);
    $: {
        console.log('the count is ' + count);
    }

	function handleClick() {
		count += 1;
	}
    
</script>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>{count} doubled is {doubled}</p>
<p>{count} tripled is {tripled}</p>

<a href="/numbers">Numbers</a>