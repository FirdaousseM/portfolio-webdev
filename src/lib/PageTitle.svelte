<script>
    const props = $props();
    const textContent = props.textContent;
</script>

<div
    id="home"
    class="flex flex-col items-center text-center gap-8 my-12 lg:my-24"
>
    <h1 class="text-6xl lg:text-8xl">{textContent.title.heading}</h1>
    <h2 class="text-4xl font-bold lg:text-6xl">
        {textContent.title.subheading}
    </h2>
</div>
