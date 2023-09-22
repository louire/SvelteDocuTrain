<script>
    import Button from './Button.svelte';

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
    <Button text ="Click Me" count = {count} on:click={handleClick}/>
    <Button text ="Reset Me" on:click={resetClick}/>
    <Button text ="Toggle Dark Mode" on:click={toggleDarkMode}/>
    
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
        Toggle DarkMode
    </button>
</div>