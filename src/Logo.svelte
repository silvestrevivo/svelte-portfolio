<script>
  import { fade } from "svelte/transition";
  import { onMount } from "svelte";
  //variables
  let visible = false;

  // lifecycle
  onMount(() => {
    setTimeout(() => {
      visible = true;
    }, 10);
  });
</script>

<style>
  img {
    width: 90%;
    height: auto;
    transition: all 0.2s ease-in-out;
  }

  img:hover {
    box-shadow: 0 0 10px #303030;
  }

  @media only screen and (max-width: 999px) and (min-width: 600px) {
    img {
      width: 500px;
    }
  }

  @media only screen and (min-width: 1000px) {
    img {
      width: 400px;
    }
  }
</style>

{#if visible}
  <img
    src="./assets/SvelteLogo.png"
    alt="SvelteLogo"
    transition:fade={{ duration: 1000 }} />
{/if}
