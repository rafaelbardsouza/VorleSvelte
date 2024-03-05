<script>
    import LandingPage from "./Components/landingPage.svelte";

</script>

<main>
	<header>
		<div class="header-container">
			<img src="./Assets/images.jpeg" alt="imagem" class="logo-image"/>
			<div class="header-ui">
			<input type="text" placeholder="o que você procura?" class="search-input"/>
			<button class="search-button">🔎</button>
			</div>
		</div>
		<div class="sub-header">
			<button class="header-button">Aplicações</button>
			<button class="header-button">Nuvoton</button>
			<button class="header-button">Parceiros</button>
		</div>
	</header>
	<LandingPage/>
</main>

<style>
    header {
        background-color: #f8f9fa;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
    }

    .header-container {
        display: flex;
        justify-content: center; 
        align-items: center;
        width: 100%;
        padding: 10px 20px;
        box-sizing: border-box;
    }

    .header-ui {
        display: flex;
        align-items: center;
        margin-left: 10px; 
    }

    .search-input {
        padding: 8px 15px;
        border: 1px solid #ced4da;
        border-radius: 20px 0 0 20px;
        margin-right: -1px; 
    }

    .logo-image {
        width: 150px; 
        height: auto;
		cursor: pointer
    }

    .header-button {
        padding: 8px 16px;
        color: #ffffff;
        font-weight: bold;
        text-transform: uppercase;
        border: 1px solid #ced4da;
        border-radius: 0 20px 20px 0;
        font-size: 1em;
		cursor: pointer
    }

	.search-button {
        color: white;
        padding: 8px 20px;
        border-radius: 0 20px 20px 0;
        margin-left: -1px;
		cursor: pointer
    }

    .sub-header {
        background-color: #1b4064;
        display: flex;
        justify-content: flex-start;
        padding: 5px 20px;
        width: 100%;
        box-sizing: border-box;
    }

    .sub-header .header-button {
        margin-right: 10px;
        border-radius: 5px;
        background-color: transparent;
        border: none;
    }
</style>