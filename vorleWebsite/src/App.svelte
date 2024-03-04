<script>
    import LandingPage from "./Components/landingPage.svelte";
	let PageHandler='LandingPage';
	function goHome(){
		PageHandler='LandingPage'
	}
</script>

<main>
	<header>
		<input type="text" placeholder="o que você procura?"/>
		<div>
			<button on:click={goHome}>Vorle</button>
			<button>Aplicações</button>
			<button>Nuvoton</button>
			<button>Parceiros</button>
		</div>
	</header>
	{#if PageHandler=='LandingPage'}
		<LandingPage/>
	{/if}
</main>

<style>

</style>