<script>
  import { fade, fly } from 'svelte/transition';
</script>

<form in:fly="{{ y: 200, duration: 3000 }}" out:fade>
  <div>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <label for="grade">Grade:</label>
    <select id="grade" name="grade" required>
      <option value="">Select a grade</option>
      <option value="9">9th</option>
      <option value="10">10th</option>
      <option value="11">11th</option>
      <option value="12">12th</option>
    </select>
    
    <label for="interests">Interests:</label>
    <textarea id="interests" name="interests" maxlength = 255></textarea>
    
    <label for="newsletter">Sign up for our newsletter:</label>
    <input type="checkbox" id="newsletter" name="newsletter">
  </div>
  <div>
    <label>What activities are you interested in? - </label>
    <input type="checkbox" id="music" name="activities" value="music">
    <label for="music">Music</label>
    
    <input type="checkbox" id="sports" name="activities" value="sports">
    <label for="sports">Sports</label>
    
    <input type="checkbox" id="coding" name="activities" value="coding">
    <label for="coding">Coding</label>
    
    <input type="checkbox" id="art" name="activities" value="art">
    <label for="art">Art</label>
  </div>
  
  <div>
    <input class="button" type="submit" value="Submit">
  </div>
</form>

<style>
  label {
    padding: var(--standard-padding);
  }
  
  form {
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

  select {
    background-color: var(--primary-background-color);
    border: var(--secondary-background-color);
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
  }

  textarea {
    background-color: var(--normal-background-color);
    border: var(--secondary-background-color);
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
    min-width: 8vw;
    max-width: 8vw;
    max-height: 1vw;
  }
  
  input {
    background-color: var(--normal-background-color);
    border: var(--secondary-background-color);
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
  }
  
  .button {
    margin-top: var(--standard-margin-width);
    width: 10vw;
    height: 2vw;
  }

  div {
    margin-bottom: var(--standard-margin-width);
  }
</style>