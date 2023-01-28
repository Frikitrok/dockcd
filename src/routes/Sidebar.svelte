<aside class="sidebar" class:closed>
  <div class="user"><div><IconButton class="material-icons">person</IconButton></div><b>Admin</b></div>
  <a class ="tab" class:selected="{current === ''}" on:click="{() => current = ''}" href="/">Main</a>
  <a class ="tab" class:selected="{current === 'pipelines'}" on:click="{() => current = 'pipelines'}" href="/pipelines">Pipelines</a>
  <a class ="tab" class:selected="{current === 'repositories'}" on:click="{() => current = 'repositories'}" href="/repositories">Repositories</a>
  <a class ="tab" class:selected="{current === 'schemas'}" on:click="{() => current = 'schemas'}" href="/schemas">Schemas</a>
  <a class ="tab" class:selected="{current === 'settings'}" on:click="{() => current = 'settings'}" href="/settings">Settings</a>
</aside>

<script>
  import IconButton from '@smui/icon-button';
  import { page } from '$app/stores';
  import { onMount } from 'svelte';
    
  export let closed = false
  export let current = "false"

  onMount(async () => {
		current = await $page.url.pathname.replace(/\//, '');
    console.log(current)
	});

</script>

<style>
  /* These classes are only needed because the
    drawer is in a container on the page. */
  .sidebar {
    top: 0;
    height: 100%;
    width: 200px;
    overflow: hidden;
    z-index: 0;
    background-color: #3a0ca3;

    display: inline-block;
    vertical-align: top;
    height: calc(100% - 63px);
    left: 0;
    width: 200px;
    overflow: auto;
    float: left;
    transition: left 0.3s ease-in-out;
  }

  .closed {
    left: -200px;
  }

  .user {
    height: 60px;
    width: 200px;
    color: white;
    font-family: Arial;
    background-color: #3B3561;
    box-shadow: 1px 1px 5px black;
  }

  .user div {
    float: left;
    margin-top: 5px;
  }

  .user b {
    display: inline-block;
    line-height: 60px;
    padding: 0;
    float: left;
    margin: 0;
  }

  .tab {
    height: 50px;
    width: 200px;
    display: block;
    background-color: rgba(0, 0, 0, 0.1);
    text-align: left;
    padding-left: 20px;
    line-height: 50px;
    color: white;
    font-family: Arial;
    text-decoration: none;
  }

  .selected {
    background-color: rgba(0, 0, 0, 0.3);
  }

  .tab:hover {
    background-color: rgba(0, 0, 0, 0.2);
  }
</style>
