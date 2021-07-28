<script>
  export let name;
  import Trendline from "./stories/Trendline.svelte";
  import Kpi from "./stories/Kpi.svelte";
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the <a href="https://github.com/Tekoma-Kft/scoreboard"
      >Scoreboard repo</a
    > to learn more.
  </p>

  <Kpi />
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
