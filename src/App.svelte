<script>
  import Logo from "./Logo.svelte";
  import ProjectsList from "./ProjectsList.svelte";
</script>

<style>
  main {
    /* border: 2px solid green; */
    height: 100%;
    display: flex;
    flex-direction: column-reverse;
    background-color: #fa3b00;
  }

  .container {
    /* border: 1px solid blue; */
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  @media only screen and (min-width: 1000px) {
    main {
      flex-direction: row;
    }
  }
</style>

<main>
  <div class="container">
    <ProjectsList />
  </div>
  <div class="container">
    <Logo />
  </div>
</main>
