<script>
  import Trendline from "./Trendline.svelte";

  const kpis = [
    {
      id: "OTD",
      name: "On-time delivery",
      emoji: "🕒",
    },
    {
      id: "SL",
      name: "Sick leave %",
      emoji: "🤒",
    },
    {
      id: "OTD",
      name: "Cap v Workload",
      emoji: "🔋",
    },
    {
      id: "OTD",
      name: "Load",
      emoji: "⌛",
    },
    {
      id: "OTD",
      name: "HDR WLD FPY",
      emoji: "👨‍🏭✔️",
    },
    {
      id: "OTD",
      name: "Blowout FPY",
      emoji: "🌬️✔️",
    },
    {
      id: "OTD",
      name: "PT FPY",
      emoji: "💥✔️",
    },
  ];

  let chart = ["📈", "📉"];

  let randomChart = chart[Math.floor(Math.random() * chart.length)];
</script>

<div class="wrapper">
  <h2 class="object-title">Production performance indicator monitoring</h2>
  <table />
  {#each kpis as kpi}
    <tr>
      <td><p class="pi">{kpi.emoji} {kpi.name}:</p> </td>
      <td><Trendline /></td>
    </tr>
  {/each}
</div>

<style>
  :root {
    --w: 50%;
  }
  .object-title {
    padding: 0.5em;
    font-family: monospace;
  }

  .wrapper {
    box-shadow: 1px 1px 3px grey;
    align-items: center;
    display: flex;
    flex-direction: column;
    align-content: space-around;
    text-align: center;
    width: 50%;
    height: var(--w);
    font-size: 2rem;
    margin: 10rem;
    border-radius: 0.1em;
    padding: 1em;
  }

  td {
    width: 20rem;
    box-shadow: 1px 1px 3px grey;
    padding-left: 2rem;
    padding-right: 2rem;
  }

  tr:nth-child(odd) {
    background-color: lightgrey;
  }
</style>
