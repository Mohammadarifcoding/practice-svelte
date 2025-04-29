<script>
	let elapsed = $state(0);
	let interval = $state(1000);

	// $effect(() => {
	// 	setInterval(()=>{
	// 		elapsed += 1;
	// 	},interval)
	// });
    $effect(() => {
        const id = setInterval(() => {
        elapsed += 1;
    },interval)    
    return ()=> clearInterval(id)
    })
    
	// $effect(() => {
	// 	const id = setInterval(() => {
	// 		elapsed += 1;
	// 	}, interval);
		
	// 	return () => clearInterval(id);
	// });
</script>

<button onclick={() => interval /= 2}>speed up</button>
<button onclick={() => interval *= 2}>slow down</button>
<p>{interval}</p>

<p>elapsed: {elapsed}</p>