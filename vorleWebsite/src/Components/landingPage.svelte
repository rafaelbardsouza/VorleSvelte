<script>
    let x = 0
    function SliderHandler(event) {
        x++
        if(x>1){
            x=0
        }
        event.preventDefault()
    }
    </script>
    
    <main>
        <div class="slider-container">
            {#if x === 0}
                <div class="content-block">
                    <button on:click={(event) => SliderHandler()} class="arrow-button">&#9664;</button>
                    <div class="text-container">
                        <h1>Suporte Nuvoton</h1>
                        <span>Em parceria com a Mastertronics, representante oficial da Nuvoton na America do Sul, a Vorle prestará suporte a linhas de microcontroladores e microprocessadores ARM e 8051 Nuvoton.</span>
                    </div>
                    <img src="./Assets/microprocessadores.jpg" alt="microprocessador" class="imagem"/>
                    <button on:click={(event) => SliderHandler()} class="arrow-button">&#9654;</button>
                </div>
            {:else}
                <div class="content-block">
                    <button on:click={(event) => SliderHandler()} class="arrow-button">&#9664;</button>
                    <div class="text-container">
                        <h1>Design for your application</h1>
                        <span>Desenvolvemos API's e bibliotecas dedicadas a sua aplicação. Otimize seu tempo de desenvolvimento, faça um orçamento!</span>
                    </div>
                    <img src="./Assets/APIs.jpeg" alt="APIs" class="imagem"/>
                    <button on:click={(event) => SliderHandler()} class="arrow-button">&#9654;</button>
                </div>
            {/if}
        </div>
    </main>

    <style>
        .slider-container {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
        }
    
        .content-block {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 16px;
            margin: 20px;
            max-width: 700px;
            transition: transform 0.3s ease-in-out;
        }
    
        .arrow-button {
            background-color: navy;
            color: #fff;
            border: none;
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            font-size: 24px;
            position: absolute;
            top: 50%;
            transform: translate(0, -50%);
            transition: background-color 0.3s ease-in-out;
        }
    
        .arrow-button:hover {
            background-color: navy;
        }
    
        .arrow-button:first-child {
            left: 20px;
        }
    
        .arrow-button:last-child {
            right: 20px;
        }
    
        .text-container {
            text-align: center;
            margin: 20px 0;
        }
    
        .content-block h1 {
            color: #007bff;
            margin-bottom: 0.5em;
        }
    
        .content-block span {
            color: #495057;
            font-size: 0.9em;
        }
    
        .content-block img {
            width: 80%;
            border-radius: 12px;
            margin-top: 1em;
        }
    </style>