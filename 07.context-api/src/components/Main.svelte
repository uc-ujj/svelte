<script>
   import Popup from "./Popup.svelte";
   
   let isPopupOpen = false
</script>
  
  <main>
    <button on:click={() => isPopupOpen = true}>Show Popup</button>
    {#if isPopupOpen}
      <Popup on:close={() => isPopupOpen = false}/>
    {/if}
  </main>
  
  <style>
    .logo {
      height: 6em;
      padding: 1.5em;
      will-change: filter;
      transition: filter 300ms;
    }
    .logo:hover {
      filter: drop-shadow(0 0 2em #646cffaa);
    }
    .logo.svelte:hover {
      filter: drop-shadow(0 0 2em #ff3e00aa);
    }
    .read-the-docs {
      color: #888;
    }
  </style>
  