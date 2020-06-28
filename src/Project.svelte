<script>
  import { fly } from "svelte/transition";
  export let name, url, index;
</script>

<li transition:fly={{ x: 500, delay: (index + 1) * 300 }}>
  <a href={url} target="_blank" rel="noopener noreferrer">{name}</a>
</li>

<style>
  li {
    list-style-type: none;
    font-size: 15px;
    margin-bottom: 10px;
    padding: 8px 20px;
    background-color: #323330;
    color: azure;
    text-transform: uppercase;
  }
  @media only screen and (min-width: 600px) {
    li {
      font-size: 20px;
    }
  }
</style>
