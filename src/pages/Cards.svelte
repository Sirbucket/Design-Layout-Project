<script>
  import { fade, fly } from 'svelte/transition';
</script>

<div class="card" in:fly="{{ y: 200, duration: 3000 }}" out:fade>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Ada_Lovelace_portrait.jpg/834px-Ada_Lovelace_portrait.jpg?20130907213703" alt="Portrait of Ada Lovelace">
  <h2>Ada Lovelace</h2>
  <p>Augusta Ada King, Countess of Lovelace was an English mathematician and writer, chiefly known for her work on Charles Babbage's proposed mechanical general-purpose computer, the Analytical Engine.</p>
  <a href="https://en.wikipedia.org/wiki/Ada_Lovelace">Read More</a>
</div>

<div class="card" in:fly="{{ y: 200, duration: 3000 }}" out:fade>
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/07/Alan_Turing_portr%C3%A9.jpg" alt="Portrait of Alan Turing">
  <h2>Alan Turing</h2>
  <p>Alan Mathison Turing was an English mathematician, computer scientist, logician, cryptanalyst, philosopher, and theoretical biologist. Turing is widely considered to be the father of theoretical computer science and artificial intelligence.</p>
  <a href="https://en.wikipedia.org/wiki/Alan_Turing">Read More</a>
</div>

<div class="card" in:fly="{{ y: 200, duration: 3000 }}" out:fade>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/Commodore_Grace_M._Hopper%2C_USN_%28covered%29.jpg/440px-Commodore_Grace_M._Hopper%2C_USN_%28covered%29.jpg">
  <h2>Grace Hopper</h2>
  <p>Grace Brewster Murray Hopper was an American computer scientist and United States Navy rear admiral. She was a pioneer of computer programming, and invented one of the first compiler related tools.</p>
  <a href="https://en.wikipedia.org/wiki/Grace_Hopper">Read More</a>
</div>

<style>

  .card {
    position: relative;
    left: 40vw;
    top: 5vw;
    width: 20vw;
    text-align: center;
    background-color: var(--primary-background-color);
    margin-bottom: var(--standard-margin-width);
    padding: var(--standard-padding);
    border-radius: var(--border-radius)
  }
  img {
    height: 10vw;
    width: 10vw;
    border: solid var(--tertiary-background-color) var(--standard-border-width);
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
    object-fit: cover;
  }

  p {
    font-size: var(--paragraph-font-size);
    background-color: var(--secondary-background-color);
    padding: var(--standard-padding);
  }

  h2 {
    font-size: var(--h2-font-size);
    background-color: var(--secondary-background-color);
    padding: var(--standard-padding);
  }

  a {
    font-size: var(--paragraph-font-size);
  }
</style>