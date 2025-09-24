<script>
    const props = $props();
    const textContent = props.textContent;
</script>

<nav class="fixed bottom-8 z-10 bg-primary w-11/12 py-6 rounded-2xl shadow-xl">
    <ul class="flex justify-around text-2xl font-bold">
        <li>
            <a href="#home">{textContent.nav.home}</a>
        </li>
        <li>
            <a href="#portfolio">{textContent.nav.portfolio}</a>
        </li>
        <li>
            <a href="#contact">{textContent.nav.contact}</a>
        </li>
    </ul>
</nav>
