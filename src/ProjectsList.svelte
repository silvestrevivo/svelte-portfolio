<script>
  import { onMount } from "svelte";
  import projectsData from "./projects/projects";
  import Project from "./Project.svelte";
  // variables
  let projects = [];

  // lifecycle
  onMount(() => (projects = projectsData));
</script>

<div class="project-list">
  {#each projects as project, index (project.id)}
    <ul>
      <Project {...project} {index} />
    </ul>
  {/each}
</div>

<style>
  .project-list {
    width: 90%;
  }

  @media only screen and (min-width: 600px) {
    .project-list {
      width: 500px;
    }
  }
</style>
