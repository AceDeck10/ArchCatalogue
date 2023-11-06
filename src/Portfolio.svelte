<script lang="ts">
import { onMount } from 'svelte';


let name : string = '';
let images: string[] = [];

onMount(() => {
    const params = new URLSearchParams(window.location.search);
    name = params.get('name') || '';

    const imageMappings: { [key: string]: string[] } = {
      'john_doe': ['john_doe_1.jpg', 'john_doe_2.jpg', 'john_doe_3.jpg', 'john_doe_4.jpg'],
      'james_roe': ['james_roe_1.jpg', 'james_roe_2.jpg', 'james_roe_3.jpg', 'james_roe_4.jpg'],
      'jane_poe': ['jane_poe_1.jpg', 'jane_poe_2.jpg', 'jane_poe_3.jpg', 'jane_poe_4.jpg'],
      'anne_cox': ['anne_cox_1.jpg', 'anne_cox_2.jpg', 'anne_cox_3.jpg', 'anne_cox_4.jpg'],
      'ben_fox': ['ben_fox_1.jpg', 'ben_fox_2.jpg', 'ben_fox_3.jpg', 'ben_fox_4.jpg'],
      'liz_day': ['liz_day_1.jpg', 'liz_day_2.jpg', 'liz_day_2.jpg', 'liz_day_4.jpg'],
      // Add mappings for other names as needed
    };

    images = imageMappings[name] || [];
  });

</script>

<div>
    <h2>{name} Portfolio</h2>

    {#if images.length > 0}
    <h2>Images:</h2>
    <ul>
        {#each images as image}
        <li><img src={`src/assets/img/${image}`} alt={image} /></li>
        {/each}
    </ul>
    {:else}
    <p>No images found for {name}.</p>
    {/if}


</div>

<style>
    
</style>