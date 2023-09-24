<script>
    import {count} from '../store/store.js';

    function handlClick() {
        count.update(n => n + 1);
    }
    
</script>

<style>
    button {
        background-color: orange;
        color: white;
        border: none;
        padding: 1em;
        border-radius: 0.5em;
        cursor: pointer;
    }
    
</style>

<button on:click={handlClick}> 
    Click {$count === 0 ? '' : $count}
</button>