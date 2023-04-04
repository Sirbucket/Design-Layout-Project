<script>
  import { fade, fly } from 'svelte/transition';
</script>
<div in:fly="{{ y: 200, duration: 3000 }}" out:fade>
  <books>Books to Read</books>
  <ol>
    <li><strong>Homegoing</strong> by Yaa Gyasi - A multi-generational story that follows the descendants of two sisters, one sold into slavery and the other married to a British slaver.</li>
    <li><strong>When Breath Becomes Air</strong> by Paul Kalanithi - A memoir by a neurosurgeon diagnosed with terminal lung cancer who reflects on life and death.</li>
    <li><strong>Beloved</strong> by Toni Morrison - A haunting novel about a former slave who escapes to Ohio but is haunted by her past.</li>
    <li><strong>The Alchemist</strong> by Paulo Coelho - A fable about a shepherd boy who embarks on a journey to fulfill his dreams.</li>
    <li><strong>The 7 Habits of Highly Effective Teens</strong> by Sean Covey - A self-help book that teaches teenagers how to become more productive and achieve their goals.</li>
  </ol>
  
  <movies>Favorite Movies</movies>
  <ul>
    <li><strong>Black Panther</strong> - Marvel's first superhero film with a predominantly black cast, set in the fictional African nation of Wakanda.</li>
    <li><strong>Crazy Rich Asians</strong> - A romantic comedy featuring an all-Asian cast that explores themes of family and cultural identity.</li>
    <li><strong>The Social Network</strong> - A drama film that depicts the founding of Facebook and the legal battles that ensued.</li>
    <li><strong>The Imitation Game</strong> - A biographical drama film about Alan Turing, a mathematician who helped crack the Enigma code during World War II.</li>
    <li><strong>The Matrix</strong> - A science fiction film that explores the concept of reality and computer simulation.</li>
  </ul>
</div>
<style>
  books {
    font-size: var(--h2-font-size);
    color: var(--primary-font-color);
    position: relative;
    top: 5vw;
    left: 42.5vw;
    width: 15vw;
    background-color: var(--primary-background-color);
    border-radius: var(--border-radius);
    border-bottom: solid var(--header-border-width) var(--secondary-background-color);
    padding: var(--standard-padding);
  }
  
  movies {
    font-size: var(--h2-font-size);
    color: var(--primary-font-color);
    position: relative;
    top: 5vw;
    left: 41.5vw;
    width: 17.5vw;
    background-color: var(--primary-background-color);
    border-radius: var(--border-radius);
    border-bottom: solid var(--header-border-width) var(--secondary-background-color);
    padding: var(--standard-padding);
  }
  
  ol {
    font-size: var(--standard-font-size);
    color: var(--primary-font-color);
    position: relative;
    top: 5vw;
    left: 17.5vw;
    width: 65vw;
    background-color: var(--primary-background-color);
    border-radius: var(--border-radius);
    border: solid var(--secondary-background-color);
    padding: var(--standard-padding);
  }
  
  ul {
    font-size: var(--standard-font-size);
    color: var(--primary-font-color);
    position: relative;
    top: 5vw;
    left: 17.5vw;
    width: 65vw;
    background-color: var(--primary-background-color);
    border-radius: var(--border-radius);
    border: solid var(--secondary-background-color);
    padding: var(--standard-padding);
  }
  
  li {
    padding: var(--standard-padding);
    margin-bottom: var(--standard-margin-width);
  }
</style>