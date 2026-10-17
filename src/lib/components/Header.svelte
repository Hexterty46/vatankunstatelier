<script>
  import logo from "#lib/assets/images/Logo.jpeg?enhanced";
</script>

<header>
  <a href="/">
    <enhanced:img src={logo} alt="Logo" />
  </a>

  <button>
    <svg
      viewBox="0 0 24 24"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
      class="svelte-1elxaub"
      width="24"
      height="24"
      ><path
        d="M4 6H20M4 12H20M4 18H20"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      ></path></svg
    >
    <span> Menu </span>
  </button>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;

    a {
      img {
        width: 100%;
        max-width: 10rem;
        height: auto;
      }
    }

    button {
      display: flex;
      flex-direction: column;
      justify-self: center;
      align-items: center;
      cursor: pointer;
      font-size: 1rem;
      background: 0 0;
      border: none;
      gap: 0.25rem;
      padding: 1rem;
    }
  }
</style>
