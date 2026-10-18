<script>
  import logo from "#lib/assets/images/footer-logo.png?enhanced";
</script>

<footer>
  <enhanced:img src={logo} alt="Footer logo" />

  <p class="tagline">Traditionele kunst met betekenis.</p>

  <nav>
    <a href="https://www.instagram.com/">
      <svg
        fill="#D8DDE3"
        viewBox="0 0 32 32"
        width="35"
        height="35"
        id="Camada_1"
        version="1.1"
        xml:space="preserve"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        stroke="#D8DDE3"
        stroke-width="0.00032"
        ><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g
          id="SVGRepo_tracerCarrier"
          stroke-linecap="round"
          stroke-linejoin="round"
        ></g><g id="SVGRepo_iconCarrier">
          <g>
            <path
              d="M22.3,8.4c-0.8,0-1.4,0.6-1.4,1.4c0,0.8,0.6,1.4,1.4,1.4c0.8,0,1.4-0.6,1.4-1.4C23.7,9,23.1,8.4,22.3,8.4z"
            ></path>
            <path
              d="M16,10.2c-3.3,0-5.9,2.7-5.9,5.9s2.7,5.9,5.9,5.9s5.9-2.7,5.9-5.9S19.3,10.2,16,10.2z M16,19.9c-2.1,0-3.8-1.7-3.8-3.8 c0-2.1,1.7-3.8,3.8-3.8c2.1,0,3.8,1.7,3.8,3.8C19.8,18.2,18.1,19.9,16,19.9z"
            ></path>
            <path
              d="M20.8,4h-9.5C7.2,4,4,7.2,4,11.2v9.5c0,4,3.2,7.2,7.2,7.2h9.5c4,0,7.2-3.2,7.2-7.2v-9.5C28,7.2,24.8,4,20.8,4z M25.7,20.8 c0,2.7-2.2,5-5,5h-9.5c-2.7,0-5-2.2-5-5v-9.5c0-2.7,2.2-5,5-5h9.5c2.7,0,5,2.2,5,5V20.8z"
            ></path>
          </g>
        </g></svg
      >
      <p>INSTAGRAM</p>
    </a>
    <a href="mailto:Kezbanarslan@yahoo.com">
      <svg
        viewBox="0 0 24 24"
        width="35"
        height="35"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        ><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g
          id="SVGRepo_tracerCarrier"
          stroke-linecap="round"
          stroke-linejoin="round"
        ></g><g id="SVGRepo_iconCarrier">
          <path
            d="M3 8L8.44992 11.6333C9.73295 12.4886 10.3745 12.9163 11.0678 13.0825C11.6806 13.2293 12.3194 13.2293 12.9322 13.0825C13.6255 12.9163 14.2671 12.4886 15.5501 11.6333L21 8M6.2 19H17.8C18.9201 19 19.4802 19 19.908 18.782C20.2843 18.5903 20.5903 18.2843 20.782 17.908C21 17.4802 21 16.9201 21 15.8V8.2C21 7.0799 21 6.51984 20.782 6.09202C20.5903 5.71569 20.2843 5.40973 19.908 5.21799C19.4802 5 18.9201 5 17.8 5H6.2C5.0799 5 4.51984 5 4.09202 5.21799C3.71569 5.40973 3.40973 5.71569 3.21799 6.09202C3 6.51984 3 7.07989 3 8.2V15.8C3 16.9201 3 17.4802 3.21799 17.908C3.40973 18.2843 3.71569 18.5903 4.09202 18.782C4.51984 19 5.07989 19 6.2 19Z"
            stroke="#D8DDE3"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          ></path>
        </g></svg
      >
      <p>E-MAIL</p>
    </a>
  </nav>
</footer>

<style>
  footer {
    background-color: var(--tertiary-background);
    padding: 2.5rem var(--spacing-m) var(--spacing-xl);
    color: #a4adb8;
    border-radius: 0 0 var(--border-radius-m) var(--border-radius-m);

    img {
      display: block;
      width: 100%;
      max-width: 9rem;
      height: auto;
    }

    .tagline {
      max-width: 10rem;
      margin-block: var(--spacing-xl) var(--spacing-2xl);
      color: #929ba7;
      font-family: Georgia, "Times New Roman", sans-serif;
      font-size: 1.2rem;
      font-style: italic;
    }

    nav {
      display: flex;
      gap: var(--spacing-xs);
      min-height: 2.75rem;
      color: inherit;
      font-size: var(--font-size-m);
      text-decoration: none;
      flex-direction: column;
      font-family: "inter", sans-serif;

      a {
        display: flex;
        align-items: center;
        gap: var(--spacing-s);
        min-height: 2.75rem;
        color: inherit;
        font-size: var(--font-size-s);
        text-decoration: none;

        svg {
          width: 2rem;
          height: 2rem;
        }
      }
    }
  }
</style>
