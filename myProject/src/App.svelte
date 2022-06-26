<script>
  let name = 'World';
  let foobar = 'black';
  const handleClick = () => {
    foobar = 'grey';
  };

  const handleInput = (e) => {
    foobar = e.target.value;
  };
</script>

<main>
  <h1>Hello {name}!</h1>
  <!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
  <p style="color: {foobar}">{foobar}</p>
  <!-- <p on:click={handleClick}>This is text update</p> -->
  <!-- two way binding -->
  <!-- <input type="text" on:input={handleInput} value={foobar} /> -->
  <!-- svelte shorthand for two way binding -->
  <input type="text" bind:value={foobar} />
  <button on:click={handleClick}>Change color</button>
</main>

<style>
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

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
