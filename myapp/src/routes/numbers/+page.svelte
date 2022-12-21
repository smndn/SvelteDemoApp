<script>
	let numbers = [1, 2];

	function addNumber() {
		numbers = [...numbers, numbers.length + 1];
		numbers = numbers;
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);

    let numbers2 = [1, 2]

    function multiplyAllNumbers2() {
        // multiply all numbers in the array
        // and return the result

        let result = 1;
        for (let i = 0; i < numbers2.length; i++) {
            result = result * numbers2[i];
        }
        
        // add result to the array
        numbers2 = [...numbers2, result];
        numbers2 = numbers2;

        let result2 = 1;
        for (let i = 0; i < numbers2.length; i++) {
            result2 = result2 * numbers2[i];
        }
        return result2;

    }
    $: product = multiplyAllNumbers2();


</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>

<p>{numbers2.join(' x ')} = {product}</p>

<button on:click={multiplyAllNumbers2}>
	Add a number
</button>

