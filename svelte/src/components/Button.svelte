<script>
    export let text;
    export let count = 0;
</script>

<button on:click >
    {text}
    {count == 0 ? '' : count}
</button>

