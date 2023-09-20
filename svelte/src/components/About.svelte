<script>
    let someText = `Data Analyst, Software Developer and a Computer Systems Engineer. I live
      in Mexico`;
    let docuText = `? es un if y : es un else`;
    let count = 0;
    function handleClick(){
        count += 1;
    }
    function resetClick(){
        count = 0;
    }
</script>

<style>
    p {
        color: var(--theme-color);
        font-size: 25px;
    }
</style>

<div class="About">
    <p>
       {someText} 
       
    </p>
    <button on:click={handleClick}>
        Click me {count == 0 ? '' : count}
    </button>
    <button on:click={resetClick}>
        Reset me
    </button>
    <p>
        {docuText}
    </p>
</div>