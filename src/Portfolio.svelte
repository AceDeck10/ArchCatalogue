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
    <div class="heading" style="display:flex; flex-direction:row;">  
      <a href="/" style="margin:1em; padding:0.5em;"><i class="fa fa-home fa-2x" aria-hidden="true"></i></a>
      <h2 style="margin:auto;">{name} Portfolio</h2>
    </div>

    {#if images.length > 0}
    <h2>&nbsp &nbsp &nbsp &nbsp &nbsp Images:</h2>
    <ul>
        {#each images as image}
        <li><img src={`./src/assets/img/${image}`} alt={image} /></li>
        {/each}
    </ul>
    {:else}
    <p>No images found for {name}.</p>
    {/if}


</div>

<style>
  .heading a {
    float: left;
    box-sizing: border-box;
    margin-left: 0.95em;
    margin-bottom: 0.5em;
    padding: 0.25em;
    color: white;
    text-decoration: underline;
    font-size: 0.85em;
  }

  .heading a:hover {
    color: darkgrey;
  }
    
</style>