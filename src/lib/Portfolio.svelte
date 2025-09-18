<script>
    import Project from "./Project.svelte";
    import projectsData from "../data/projects.json";
    let projects = projectsData.projects;

    const props = $props();
    const textContent = props.textContent;
</script>

<h2 id="portfolio" class="text-6xl mb-12">{textContent.projects.heading}</h2>
<div class="flex flex-col items-center gap-32">
    {#each projects as project}
        <Project {project}></Project>
    {/each}
</div>
