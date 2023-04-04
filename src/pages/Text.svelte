<script>
  import { fade, fly } from 'svelte/transition';
</script>

<div in:fly="{{ y: 200, duration: 3000 }}" out:fade>
  <h1>The History of Typography</h1>
  
  <p>Typography has a rich and fascinating history, from the earliest handwritten manuscripts to the digital fonts we use today. But typography isn't just about aesthetics; it's also about communication and legibility.</p>
  
  <p>One of the most important considerations in typography is <em>line height</em>. This refers to the amount of space between each line of text. If the line height is too small, the text can be hard to read; if it's too large, it can be difficult to follow the flow of the text. The optimal line height depends on the font size, but a good rule of thumb is to set it to around 1.5 times the font size.</p>
  
  <p><strong>Alignment</strong> is another important aspect of typography. Text can be aligned to the left, right, center, or justified (where both the left and right edges are aligned). Different alignments can create different moods and visual effects. For example, centered text can feel more formal and balanced, while left-aligned text can feel more casual and informal.</p>
  
  <p><em>Responsive design</em> is a relatively new consideration in typography, but it's becoming increasingly important as more and more people use mobile devices to access the internet. Responsive typography involves designing fonts that can adapt to different screen sizes and resolutions. This can involve using different font sizes, line heights, and even different fonts for different devices.</p>
  
  <p>Overall, typography is a complex and ever-evolving field, but it's essential for effective communication and visual design. By understanding the history and principles of typography, you can create more effective and impactful designs for all kinds of projects.</p>
  
  <h2>Examples of Typography Elements</h2>
  
  <h3>Headings</h3>
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <h3>Heading 3</h3>
  <h4>Heading 4</h4>
  <h5>Heading 5</h5>
  <h6>Heading 6</h6>
  
  <h3>Block Quotes</h3>
  <blockquote>
    "The secret of getting ahead is getting started." -Mark Twain
  </blockquote>
  
  <h3>Lists</h3>
  <h4>Ordered List</h4>
  <ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ol>
  
  <h4>Unordered List</h4>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
  
  <h3>Formatting</h3>
  <p><strong>Bold text</strong> and <em>Italic text</em></p>
</div>

<style>
  div {
    position: relative;
    top: 5vw;
    background-color: var(--primary-background-color);
    border-radius: var(--border-radius);
    margin-bottom: var(--standard-margin-width);
    padding: var(--standard-padding);
    text-align: justify;
  }
  h1 {
    text-size: var(--h1-font-size);
    border-bottom: solid var(--tertiary-background-color) var(--header-margin-width);
  }
  h2 {
    text-size: var(--h2-font-size);
    border-bottom: solid var(--tertiary-background-color) var(--header-margin-width);
  }
  h3 {
    text-size: var(--h3-font-size);
    border-bottom: solid var(--tertiary-background-color) var(--header-margin-width);
  }
  h4 {
    text-size: var(--h4-font-size);
    border-bottom: solid var(--tertiary-background-color) var(--header-margin-width);
  }
  h5 {
    text-size: var(--h5-font-size);
    border-bottom: solid var(--tertiary-background-color) var(--header-margin-width);
  }
  h6 {
    text-size: var(--h6-font-size);
    border-bottom: solid var(--tertiary-background-color) var(--header-margin-width);
  }
  p {
    text-size: var(--paragraph-font-size);
  }
  blockquote {
    text-size: var(--standard-font-size);
  }
</style>