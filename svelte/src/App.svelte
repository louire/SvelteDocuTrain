<script>
  export let name;
  export let lastname;
</script>

<body>
  <main>
    <h1>Hello {name} {lastname}!</h1>
    <h2>Alv ya se svelte</h2>
    <p>
      Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
      how to build Svelte apps.
    </p>
  </main>
</body>

<style>
  /* Las funciones globales de css aplica a todo lo que no se le especifica */
  :global(body) {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
      Roboto, Ubuntu, "Helvetica Neue", sans-serif;
    background-color: #f2eee2;
    color: #0084f6;
  }
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
  h2 {
    color: black;
    text-transform: uppercase;
    font-size: 2em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
