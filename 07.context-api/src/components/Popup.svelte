<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
</script>

<main>
    <button on:click={() => dispatch('close')}>Close Popup</button>
    <h2>Popup Opened</h2>
</main>
