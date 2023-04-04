# Instructions  
Your job is to create a clear design language so that this set of examples feels coherent and beautiful. I encourage you to use:

* CSS Variables
* Components

You should pay special attention to:
* Padding/Margins/Spacing
* Typography (fonts, font sizes, font weights)
* Color

You might take inspiration from major design systems such as Material Design (google), Bootstrap (twitter), W3.CSS or Tailwind to see how people go about things like setting margins and such.

You are also welcome to use app.css to insert vanilla CSS into your project.

## CSS Variables

### Starting with Colors

Here's a little lesson on CSS variables in svelte I generated with ChatGPT for you:

#### 1. Define your CSS Variables 
Define your CSS variables in a :root selector in your App.svelte file:
```svelte
:root {
  --primary-color: #007bff;
  --primary-text-color: #fff;
  --secondary-color: #6c757d;
  --secondary-text-color: #fff;
}
```
#### 2. Use the variables
Use the CSS variables in your components:
```svelte
<style>
  form {
    background-color: var(--primary-color);
    color: var(--primary-text-color);
  }
</style>

<form>
  <!-- form content here -->
</form>
```

```svelte
<style>
  .card {
    background-color: var(--secondary-color);
    color: var(--secondary-text-color);
  }
</style>

<div class="card">
  <!-- card content here -->
</div>
```

This way, you can define your CSS variables once and use them across multiple components while ensuring that there is enough contrast between the background color and the text color.

## Adding Spacing

Define your CSS variables in a :root selector in your App.svelte file:

```svelte
:root {
  --base-font-size: 16px;
  --base-line-height: 1.5;
  --base-spacing-unit: 8px;
}
Use the CSS variables to set up basic sizing, padding, and margins in your components:
<!-- form.svelte -->
<style>
  form {
    font-size: var(--base-font-size);
    line-height: var(--base-line-height);
    padding: var(--base-spacing-unit);
    margin-bottom: var(--base-spacing-unit);
  }
</style>
```

```svelte
<form>
  <!-- form content here -->
</form>
```

```svelte
<!-- card.svelte -->
<style>
  .card {
    font-size: calc(var(--base-font-size) * 1.25);
    line-height: var(--base-line-height);
    padding: calc(var(--base-spacing-unit) * 2);
    margin-bottom: var(--base-spacing-unit);
  }
</style>

<div class="card">
  <!-- card content here -->
</div>
```

This way, you can define your CSS variables once and use them across multiple components while ensuring that your sizing, padding, and margins are consistent.

### Referencing Variables in App.css

You can also define (or reference) variables in app.css if you prefer. This could be helpful in setting up our generic "reset" for the project:


```svelte
/* app.css */
html {
  font-size: var(--base-font-size);
  line-height: var(--base-line-height);
}

body {
  margin: 0;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  margin-top: 0;
  margin-bottom: calc(var(--base-spacing-unit) * 2);
}

input,
button {
  font-size: inherit;
  padding: var(--base-spacing-unit);
}

button {
  border: none;
  background-color: transparent;
}
```