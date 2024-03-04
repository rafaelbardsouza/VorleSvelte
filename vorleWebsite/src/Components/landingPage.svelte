<script>
let x=0;
function SliderHandler(){
    x++;
    if(x>1){
        x=0
    }
}   

</script>

<main>
    <div>
        {#if x == 0}
            <h1>Suporte Nuvoton</h1>
        {:else}
            <h1>Design for your application</h1>
        {/if}
        <button on:click={SliderHandler}/>
        <button on:click={SliderHandler}/>
    </div>
</main>

<style></style>