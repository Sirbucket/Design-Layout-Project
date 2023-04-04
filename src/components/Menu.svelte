<script>
  let open = false
</script>


<div class="menu">
  <button on:click={()=>open=true}>
    ☰
  </button>
    {#if open}
      <ul on:click={()=>open=false}>
        <slot/>
      </ul>
      <div class="click-catcher" on:click={()=>open=false}>
      </div>
    {/if}
</div>

<style>
  .menu {
    position: relative;
    top: 0.5vw;
    left: 2vw;
  }
  ul {
    position: absolute;
    background-color: var(--primary-background-color);
    border: var(--standard-border-width) solid;
    border-radius: var(--border-radius);
    z-index: 2;
    top: 0;
    left: 0;
    padding: 0;
  }
  .click-catcher {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    z-index: 1;
  }
  button {
    width: min(5vw, 64px);
    height: min(5vw, 64px);
    justify-content: center;
    text-align: center;
    font-size: var(--h1-font-size);
    background-color: var(--primary-background-color);
    border-radius: var(--border-radius);
  }
  
</style>
