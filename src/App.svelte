<script>
  import Logo from "./Logo.svelte";
  import Disclaimer from "./Disclaimer.svelte";
  import ProjectsList from "./ProjectsList.svelte";
</script>

<style>
  main {
    height: 100vh;
  }

  .container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 25px 0;
  }

  @media only screen and (min-width: 1000px) {
    main {
      flex-direction: row;
      display: flex;
    }
  }
</style>

<main>
  <div class="container">
    <Logo />
  </div>
  <div class="container">
    <ProjectsList />
  </div>
  <Disclaimer />
</main>
