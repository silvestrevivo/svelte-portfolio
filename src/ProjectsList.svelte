<script>
  import projectsData from "./projects/projects";
  import Project from "./Project.svelte";
</script>

<style>
  .project-list {
    width: 90%;
  }
  .loading {
    color: azure;
    font-size: 25px;
  }

  @media only screen and (min-width: 600px) {
    .project-list {
      width: 500px;
    }
  }
</style>

<div class="project-list">
  {#each projectsData as project (project.id)}
    <ul>
      <Project {...project} />
    </ul>
  {:else}
    <p class="loading">loading...</p>
  {/each}
</div>
