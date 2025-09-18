<script>
    const props = $props();
    const project = props.project;
</script>

<div class="flex flex-col w-2/3 items-center">
    <img class="size-80" src="https://picsum.photos/200" alt="project" />

    <div class="flex flex-col items-center gap-4">
        <a href={project.sublink} class="text-4xl font-bold">{project.title}</a>
        <p class="overflow-ellipsis">{project.description}</p>
        <div class="flex gap-2">
            {#each project.stack as techno}
                <span class="bg-primary rounded-4xl px-3 py-1">
                    {techno}
                </span>
            {/each}
        </div>
    </div>
</div>
