<script>
  import logo from '#lib/assets/images/new-logo.png?enhanced'

  let menuOpen = $state(false)
</script>

<header>
  <a href="/">
    <enhanced:img src={logo} alt="Website logo" />
  </a>

  <a class="menu-button" href="#menu" aria-expanded={menuOpen} onclick={(event) => {event.preventDefault(); menuOpen = true}}>
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

  <nav class="menu" class:is-open={menuOpen} id="menu">
    <a class="menu-close" href="#" onclick={(event) => {event.preventDefault(); menuOpen = false}}>
              <svg viewBox="0 0 32 32" width="32" height="32">
            <title>Sluiten</title>
            <path
              d="M31.708 25.708c-0-0-0-0-0-0l-9.708-9.708 9.708-9.708c0-0 0-0 0-0 0.105-0.105 0.18-0.227 0.229-0.357 0.133-0.356 0.057-0.771-0.229-1.057l-4.586-4.586c-0.286-0.286-0.702-0.361-1.057-0.229-0.13 0.048-0.252 0.124-0.357 0.228 0 0-0 0-0 0l-9.708 9.708-9.708-9.708c-0-0-0-0-0-0-0.105-0.104-0.227-0.18-0.357-0.228-0.356-0.133-0.771-0.057-1.057 0.229l-4.586 4.586c-0.286 0.286-0.361 0.702-0.229 1.057 0.049 0.13 0.124 0.252 0.229 0.357 0 0 0 0 0 0l9.708 9.708-9.708 9.708c-0 0-0 0-0 0-0.104 0.105-0.18 0.227-0.229 0.357-0.133 0.355-0.057 0.771 0.229 1.057l4.586 4.586c0.286 0.286 0.702 0.361 1.057 0.229 0.13-0.049 0.252-0.124 0.357-0.229 0-0 0-0 0-0l9.708-9.708 9.708 9.708c0 0 0 0 0 0 0.105 0.105 0.227 0.18 0.357 0.229 0.356 0.133 0.771 0.057 1.057-0.229l4.586-4.586c0.286-0.286 0.362-0.702 0.229-1.057-0.049-0.13-0.124-0.252-0.229-0.357z"
            ></path>
          </svg>
    </a>
    <ul>
      <li><a href="/Werk" onclick={() => (menuOpen = false)}>Werk</a></li>
      <li><a href="/Over-mij" onclick={() => (menuOpen = false)}>Over mij</a></li>
      <li><a href="/Participaties" onclick={() => (menuOpen = false)}>Participaties</a></li>
      <li><a href="/Portfolio" onclick={() => (menuOpen = false)}>Portfolio</a></li>
      <li><a href="/Kunst-vormen" onclick={() => (menuOpen = false)}>Kunst vormen</a></li>
      <li><a href="/Het-atelier" onclick={() => (menuOpen = false)}>Het atelier</a></li>
      <li><a href="/Exposities" onclick={() => (menuOpen = false)}>Exposities</a></li>
      <li><a href="/Cursussen" onclick={() => (menuOpen = false)}>Cursussen</a></li>
      <li><a href="/Contact" onclick={() => (menuOpen = false)}>Contact</a></li>
    </ul>
  </nav>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;

    a {
      img {
        width: 100%;
        max-width: 8.5rem;
        height: auto;
      }
    }

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
    }

      .menu-button {
        background-color: var(--blue);
        color: black;
        text-decoration: none;
        padding: .2rem .5rem;
        border-radius: .5rem;
      }

      nav {
        background-color: var(--secondary-background);
        width: 15rem;
        height: 100vw;
        display: flex;
        flex-direction: column;
        translate: -102%;
        position: fixed;
        top: 0;
        left: 0;
        interactivity: inert;

        @media (prefers-reduced-motion: no-preference) {
          transition: .3s ease;
        }

        .menu-close {
          align-self: flex-end;
          padding: 1rem 1rem 0 0;
        }

        ul {
          padding: 0;
          margin: 0;
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

        &:target,
        &.is-open {
          translate: 0;
          interactivity: auto;
        }
      }
  }
</style>
