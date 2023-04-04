<script lang="ts">
  let active = false;
  import Tab from './components/Tab.svelte';
  import Tabs from './components/Tabs.svelte';
  import Menu from "./components/Menu.svelte";
  import Grid from './pages/Grid.svelte';
  import Cards from './pages/Cards.svelte';
  import Lists from './pages/Lists.svelte';
  import Form from './pages/Form.svelte';
  import Text from './pages/Text.svelte';
  let pages = [
    'Grid',
    'Lists',
    'Form',
    'Text',
    'Cards'
  ]
  let page = 'Grid'
</script>

<header>
  <div>
    <Menu>
      {#each pages as p}
        <Tab
          active={page==p} 
          on:click={()=>page=p}
        >
        {p}
        </Tab>
      {/each}
    </Menu>
    <Tabs>
      {#each pages as p}      
        <Tab 
          active={page==p} 
          on:click={()=>page=p}
        >
          {p}
        </Tab>
      {/each}    
    </Tabs>
  </div>
  <h1>My Design Demo</h1>
</header>
<main>
  {#if page=='Grid'}
    <Grid/>
  {:else if page=='Lists'}
    <Lists/>
  {:else if page=='Text'}
    <Text/>
  {:else if page=='Form'}
    <Form/>  
  {:else if page=='Cards'}
    <Cards/>
  {/if}
</main>

<style>
  div {
    position: absolute;
    width: 100vw;
    height: 5vw;
    top: 0;
    left: 0;
    background-color: var(--secondary-background-color);
  }
  
  main {
    justify-content: center;
  }
  h1 {
    background-color: var(--secondary-background-color);
    margin-bottom: var(--standard-header-margin-width);
    position: relative;
    left: 40vw;
    top: 5vw;
    width: 20vw;
    text-align: center;
    font-size: var(--h1-font-size);
    padding: var(--standard-padding);
    border-bottom: var(--header-border-width) solid var(--tertiary-background-color);
    border-radius: var(--border-radius);
    margin-bottom: var(--standard-margin-width);
    justify-content: center;
  }

  p {
    color: var(--secondary-font-color);
  }
</style>
