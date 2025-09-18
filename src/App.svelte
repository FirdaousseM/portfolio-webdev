<script>
  import Contact from "./lib/Contact.svelte";
  import MenuNav from "./lib/MenuNav.svelte";
  import PageTitle from "./lib/PageTitle.svelte";
  import Portfolio from "./lib/Portfolio.svelte";
  import textData from "./data/textContent.json";
  const textContent = textData.french;
</script>

<main class="w-svw h-svh flex flex-col items-center">
  <MenuNav {textContent}></MenuNav>
  <PageTitle {textContent}></PageTitle>
  <Portfolio {textContent}></Portfolio>
  <Contact {textContent}></Contact>
</main>
