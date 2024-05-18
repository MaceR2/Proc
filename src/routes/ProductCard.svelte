<script>
  import { createEventDispatcher } from 'svelte';

  export let product;

  const dispatch = createEventDispatcher();

  function buy() {
    dispatch('buy', { id: product.id });
  }
</script>

<div class="product-card">
  <h3>{product.name}</h3>
  <p>{product.description}</p>
  <p>Цена: {product.price}</p>
  <button on:click={buy}>Купить</button>
</div>

<style>
  .product-card {
    border: 1px solid #9009ff;
    border-radius: 8px;
    padding: 1rem;
    margin: 0.5rem;
    max-width: 300px;
  }

  
</style>
