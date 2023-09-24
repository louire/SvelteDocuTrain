<script>

  import { onMount } from "svelte";
    let photos = [];



    onMount(async () =>{
        console.log('onMount')
        const response = await fetch('http://jsonplaceholder.typicode.com/photos?_limit=10') 
        photos = await response .json();   
    })
</script>

<style>
    .Photos{
        width: 100%;
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        grid-gap: 1em;

    }
</style>



<div class="Photos">
    {#each photos as photo}
         <!-- content here -->
         <figure>
            <img src={photo.thumbnailUrl} alt={photo.title} />
            <figcaption>{photo.title}</figcaption>
         </figure>
    {:else}
         <p>
            Loading...
         </p>
    {/each}
</div>








