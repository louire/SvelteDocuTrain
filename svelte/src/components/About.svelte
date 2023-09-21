<script>
    let someText = `Data Analyst, Software Developer and a Computer Systems Engineer. I live
      in Mexico`;
    let docuText = `? es un if y : es un else`;
    let count = 0;

    let styles = {darkMode : false};

    function handleClick(){
        count += 1;
    }
    function resetClick(){
        count = 0;
    }
    function toggleDarkMode(){
        styles.darkMode = !styles.darkMode;
        //! significa negacion 
        window.document.body.classList.toggle("dark-mode");
    }
</script>

<style>
    p {
        color: var(--theme-color);
        font-size: 25px;
    }
</style>

<div class="About">
{#if !styles.darkMode}
    <p> {someText} </p>
{:else}
    <p>
        <span>Hello Dark mode</span>
    </p>
{/if}

    
    <button on:click={handleClick}>
        Click me {count == 0 ? '' : count}
    </button>
    <button on:click={resetClick}>
        Reset me
    </button>
    <p>
        {docuText}
    </p>
    <button on:click={toggleDarkMode}>
        Toggle Dark Mode
    </button>
</div>