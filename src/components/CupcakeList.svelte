<script lang="ts">
    import CupcakeItem from './CupcakeItem.svelte';
    import { color, cupcakes } from '../stores';
    import style from 'svelte-inline-css';
</script>

<div class="divide-dashed divide-y mb-auto px-4">
    {#each $cupcakes as cupcake}
    <div use:style={{ borderColor: $color.text }}>
        <CupcakeItem {cupcake}></CupcakeItem>
    </div>
    {/each}
</div>