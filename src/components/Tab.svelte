<script>
  export let active;
</script>

<li class:active class="tab" on:click>
  <slot/>
</li>

<style>
  li {
    background-color: var(--normal-background-color);
    border-bottom: var(--standard-border-width) solid var(--normal-background-color);
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
    list-style: none;
  }
  li .hover {
    background-color: var(--primary-background-color);
    transform: scale(1.1);
  }
  
  li.active {
    border-bottom: 1px solid var(--tertiary-background-color);
    background-color: var(--primary-background-color);
    font-weight: bold;
  }
</style>
  