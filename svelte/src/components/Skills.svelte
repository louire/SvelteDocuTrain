<!--
    each controls the iteration of a list
-->

<script>
    let skills = [
        {
            id: 1,
            name: 'Python'
        },
        {
            id: 2,
            name: 'Rust'
        },
        {
            id: 3,
            name: 'C#'
        }
    ]
</script>

<style>
    .Skills{
        display: flex;
        align-items: center;
        justify-content: center;
    }
    ul{
        margin: 0;
        padding: 0;
        list-style: none;
    }
    li{
        margin: 0 1em;
        padding: 0.5em 1em;
        border: 1px solid #ccc;
        border-radius: 5px;
    }
</style>



<div class="Skills">
    <h3>Habilidades</h3>
    <ul>
    {#each skills as skill, i }
        <li>{skill.name}</li>
    {/each}
    </ul>
</div>

