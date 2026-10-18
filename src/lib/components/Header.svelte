<script>
  import logo from "#lib/assets/images/new-logo.png?enhanced"

  let menuOpen = $state(false)
</script>

<header>
  <a
    class="menu-button"
    href="#menu"
    onclick={(event) => {
      event.preventDefault()
      menuOpen = true
    }}
  >
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
  </a>

  <a href="/">
    <enhanced:img src={logo} alt="Website logo" />
  </a>

  <nav class="menu" class:is-open={menuOpen} id="menu">
    <a
      class="menu-close"
      href="#"
      onclick={(event) => {
        event.preventDefault()
        menuOpen = false
      }}
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        class="lucide lucide-x"
        data-loc="client/src/pages/Home.tsx:107"
        ><title>Sluiten</title><path d="M18 6 6 18"></path><path d="m6 6 12 12"
        ></path></svg
      >
    </a>
    <ul>
      <li><a href="/Werk" onclick={() => (menuOpen = false)}>Werk</a></li>
      <li>
        <a href="/Over-mij" onclick={() => (menuOpen = false)}>Over mij</a>
      </li>
      <li>
        <a href="/Participaties" onclick={() => (menuOpen = false)}
          >Participaties</a
        >
      </li>
      <li>
        <a href="/Portfolio" onclick={() => (menuOpen = false)}>Portfolio</a>
      </li>
      <li>
        <a href="/Kunst-vormen" onclick={() => (menuOpen = false)}
          >Kunst vormen</a
        >
      </li>
      <li>
        <a href="/Het-atelier" onclick={() => (menuOpen = false)}>Het atelier</a
        >
      </li>
      <li>
        <a href="/Exposities" onclick={() => (menuOpen = false)}>Exposities</a>
      </li>
      <li>
        <a href="/Cursussen" onclick={() => (menuOpen = false)}>Cursussen</a>
      </li>
      <li><a href="/Contact" onclick={() => (menuOpen = false)}>Contact</a></li>
    </ul>
  </nav>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;
    background-color: var(--background-primary);

    /* Logo */
    a:nth-of-type(2) {
      img {
        width: 100%;
        max-width: 8.5rem;
        height: auto;
      }
    }

    /* Menu knop */
    a {
      display: flex;
      flex-direction: column;
      justify-self: center;
      align-items: center;
      cursor: pointer;
      font-size: var(--font-size-s);
      background: 0 0;
      border: none;
      gap: var(--spacing-2xs);
      padding: var(--spacing-m);
      color: black;
    }

    /* Navigatie menu */
    .menu {
      background-color: var(--secondary-background);
      width: 10rem;
      height: fit-content;
      max-height: 100%;
      display: flex;
      flex-direction: column;
      translate: -102%;
      position: fixed;
      top: 0;
      left: 0;
      interactivity: inert;

      @media (prefers-reduced-motion: no-preference) {
        transition: 0.3s ease;
      }

      /* Menu sluiten knop */
      .menu-close {
        align-self: flex-end;
        padding: 1rem 1rem 0 0;
        color: black;
      }

      ul {
        li {
          list-style-type: none;
          a {
            display: flex;
            color: var(--blue);
            text-decoration: none;
            font-weight: bold;
            padding: 1rem;

            &:hover {
              background-color: var(--blue);
              color: var(--green);
            }
          }
        }
      }

      &.is-open {
        translate: 0;
        interactivity: auto;
      }
    }
  }
</style>
