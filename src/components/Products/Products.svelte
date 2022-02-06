<script>
  import { onMount, onDestroy } from "svelte";
  import products from "../../stores/defaultProducts";

  let localProducts = [];
  onMount(() => {
    products.subscribe((value) => {
      localProducts = value;
    });
  });
</script>

<h1>Products Component</h1>

{#each localProducts as product}
  <!-- content here -->
  <h2>{product.title}</h2>
{/each}
