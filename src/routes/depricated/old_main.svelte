<script>
  import Header from './Header.svelte';
  import Nested from './Nested.svelte';
  import Info from './Info.svelte';
	let name = 'world';
  let src = '/dock_logo.webp';

  let count = 0;
  $: doubled = count * 2;
  function incrementCount() {
	  count += 1;
  }
  
  $: {
	  console.log('the count is ' + count);
  }

  const pkg = {
		name: 'svelte',
		version: 3,
		speed: 'blazing',
		website: 'https://svelte.dev'
	};
</script>

<Header/>

<h1>Welcome {name.toUpperCase() }</h1>
<img {src} alt="A man dances." style="height: 200px;">
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<p>This is a paragraph.</p>

<style>
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>

<Nested answer={42}/>
<Info {...pkg}/>

<button on:click={incrementCount}>Clicked {count} {count === 1 ? 'time' : 'times'}</button>
<p>{count} doubled is {doubled}</p>