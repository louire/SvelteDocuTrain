<script>
  import About from "./components/About.svelte";
  import Person from "./components/Person.svelte";
  import Text from "./components/Text.svelte";
  export let name;
  export let lastname;
  let gatoLoco = "https://i.imgur.com/9bxvv1N.jpg";
  let smurfCat = "https://i.imgur.com/de1BULN.jpeg";
  
  const data = {
    name: "Loui",
    lastName: "Recio",
    age: 23
  }

</script>


<style>
  /* Las funciones globales de css aplica a todo lo que no se le especifica */
  :global(body) {
    color: #0084f6;
  }
  :global(:root) {
    --theme-color: purple;
    --img-width: 30%;
    --img-height: auto;
  }

  :global(body.dark-mode) {
    background-color: #1d3040;
    color: #bfc2c7;
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


<body>
  <main>
    <h1>Hello {name} {lastname}!</h1>
    <h2>Alv ya se svelte</h2>
    <About />
    <Text anotherText="Otro texto" />
    <Person {...data} />
    <img src={gatoLoco} alt="Una foto de un Gato que esta loco" />
    <img src={smurfCat} alt="Una foto de un GatoPitufo que esta loco" />
  </main>
</body>