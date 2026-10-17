<script>
  const isDev = import.meta.env.DEV
</script>

{#if isDev}
  <div class="dev-banner">🔴 Dev</div>
{/if}

<style>
  .dev-banner {
    position: fixed;
    right: 0;
    bottom: 0;
    z-index: 9999;
    padding: 8px 16px;
    color: #222;
    font-weight: bold;
    font-size: 12px;
    border-bottom-left-radius: 8px;
  }
</style>
