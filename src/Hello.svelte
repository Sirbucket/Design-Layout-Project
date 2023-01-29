<script>
  import svelteLogo from "./assets/svelte.svg";
  import { fade, fly } from "svelte/transition";
  import { onMount } from "svelte";
  let ready = false;
  onMount(() => (ready = true));
</script>

<div>
  <h1>
    {#if ready}<img
        in:fade={{ duration: 2000, delay: 500 }}
        alt="Svelte Logo"
        src={svelteLogo}
      />{/if}
    Hello Svelte
  </h1>
  {#if ready}
    <p in:fly={{ x: -400, duration: 1000, delay: 250 }}>
      <a href="https://svelte.dev/tutorial/basics" target="_BLANK">
        Learn Svelte from the Official Tutorial!
      </a>
    </p>
  {/if}
</div>

<style>
  img {
    height: 1em;
    position: relative;
    top: 0.25em;
    left: 0.25em;
  }
  div {
    width: 100vw;
    height: 100vh;
    display: grid;
    place-content: center;
    font-size: 2em;
    text-align: center;
  }
</style>
