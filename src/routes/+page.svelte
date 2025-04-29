<script>
	import NewScript from '../script/newScript.svelte';
    import Effect from '../script/effect.svelte';
	let name = 'Learning svelte';
	let src = 'https://avatars.githubusercontent.com/u/113016314?v=4';
	let string = `this string contains some <strong>HTML!!!</strong>`;
    let count = $state(1)
    let secondCount = $state(1)
    let total = $derived(count + secondCount)
   


    function increment(){
        count++
    }
    function increment2(){
        secondCount++
    
    }

    $inspect(count,secondCount).with(console.trace)
</script>


<!-- <h1 class="text-3xl font-bold underline">{name.toUpperCase()}</h1>
<img {src} alt="{name} profile image of mine" />
<p>{@html string}</p>
<p class="p-4 border text-2xl">Count : {count} {secondCount}  Total : {total} </p>

<button onclick={increment}>Add+</button>
<button onclick={increment2}>Add+</button> -->

<!-- <NewScript /> -->
<Effect/>
<style>
	img {
		border-radius: 50%;
	}
</style>
