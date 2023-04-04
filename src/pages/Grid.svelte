<script>
  import { fade, fly } from 'svelte/transition';
</script>

<table in:fly="{{ y: 200, duration: 3000 }}" out:fade>
  <thead>
    <tr>
      <th>Date</th>
      <th>Day of Week</th>
      <th>Temperature</th>
      <th>Condition</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>March 28, 2023</td>
      <td>Monday</td>
      <td>64°F</td>
      <td>Partly cloudy</td>
    </tr>
    <tr>
      <td>March 29, 2023</td>
      <td>Tuesday</td>
      <td>60°F</td>
      <td>Mostly sunny</td>
    </tr>
    <tr>
      <td>March 30, 2023</td>
      <td>Wednesday</td>
      <td>68°F</td>
      <td>Partly cloudy</td>
    </tr>
    <tr>
      <td>March 31, 2023</td>
      <td>Thursday</td>
      <td>72°F</td>
      <td>Sunny</td>
    </tr>
    <tr>
      <td>April 1, 2023</td>
      <td>Friday</td>
      <td>69°F</td>
      <td>Scattered thunderstorms</td>
    </tr>
  </tbody>
</table>

<style>
  table {
    font-size: var(--standard-font-size);
    color: var(--primary-font-color);
    position: relative;
    top: 5vw;
    left: 32.5vw;
    width: 35vw;
    background-color: var(--primary-background-color);
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
  }
  thead {
    background-color: var(--tertiary-background-color);
    text-align: center;
  }
  tbody {
    background-color: var(--secondary-background-color);
    text-align: center;
  }
  td {
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
  }
  th {
    border-radius: var(--border-radius);
    padding: var(--standard-padding);
  }
</style>

