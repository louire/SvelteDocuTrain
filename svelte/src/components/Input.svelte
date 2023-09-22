<script>
    export let name = "World";
</script>

<div class="Input">
    <input type="text" placeholder="Enter your name here" bind:value={name}/>
    <p>Hello {name}!</p>

</div>
