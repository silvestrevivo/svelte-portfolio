<script>
  import { fly } from "svelte/transition";
  import { onMount } from "svelte";
  //variables
  let visible = false;

  // lifecycle
  onMount(() => (visible = true));
</script>

{#if visible}
  <footer transition:fly={{ y: 100, duration: 2000, delay: 500 }}>
    <a href="https://github.com/silvestrevivo" target="_blank">
      <i class="fab fa-github" />
    </a>
    <a href="https://twitter.com/silvestrevivo" target="_blank">
      <i class="fab fa-twitter" />
    </a>
    <a
      href="https://www.linkedin.com/in/silvestre-vivo-1a6843bb/"
      target="_blank">
      <i class="fab fa-linkedin" />
    </a>
    <a href="https://www.reddit.com/user/silvestrevivo/" target="_blank">
      <i class="fab fa-reddit" />
    </a>
  </footer>
{/if}

<style>
  footer {
    text-align: center;
    color: azure;
    padding: 10px;
  }

  a {
    margin: 0 5px;
    font-size: 25px;
    transition: all 0.1s ease-in-out;
  }

  a:hover {
    color: #fd997a;
  }

  @media only screen and (min-width: 1000px) {
    footer {
      position: absolute;
      right: 0;
      bottom: 0;
      width: 100%;
    }
  }
</style>
