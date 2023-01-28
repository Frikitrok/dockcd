<script>
  import Header from './Header.svelte';
  import Sidebar from './Sidebar.svelte';

  let closed = false
</script>

<Header bind:sidebar={closed}/>
<Sidebar bind:closed/>


<slot></slot>

<style>
  :global(html) {
    height: 100%;
	}

  :global(body) {
    margin: 0px;
    padding: 0px;
    height: 100%;
	}
</style>
