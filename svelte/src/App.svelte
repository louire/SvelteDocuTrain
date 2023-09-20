<script>
  import About from "./components/About.svelte";
  export let name;
  export let lastname;
  let gatoLoco = "https://i.imgur.com/9bxvv1N.jpg";
  let smurfCat = "https://i.imgur.com/de1BULN.jpeg";
</script>

<body>
  <main>
    <h1>Hello {name} {lastname}!</h1>
    <h2>Alv ya se svelte</h2>
    <About />
    <img src={gatoLoco} alt="Una foto de un Gato que esta loco" />
    <img src={smurfCat} alt="Una foto de un GatoPitufo que esta loco" />
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
  :global(:root) {
    --theme-color: purple;
    --img-width: 30%;
    --img-height: auto;
  }

  

  /* Las variables de css solo aplican a lo que se le especifica */

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
  main img {
    width: var(--img-width);
    height: var(--img-height);
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
