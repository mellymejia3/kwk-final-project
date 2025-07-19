<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  //data for chart
  const series = [
    {
      name: "Group 1",
      data: [
        [1990, 3],
        [2000, 4],
        [2010, 1],
        [2020, 1],
      ],
      color: "#8427c9",
    },
    {
      name: "Group 2",
      data: [
        [1990, 2],
        [2000, 5],
        [2010, -2],
        [2020, 2],
      ],
      color: "#ff99fc",
    },
    {
      name: "Group 3",
      data: [
        [1990, 4],
        [2000, 3],
        [2010, 0],
        [2020, 3],
      ],
      color: "#4096fa",
    },
  ];

  let chart;
  let thirdSeriesVisible = false;

  let options = {
    chart: {
      type: "spline",
      backgroundColor: "#e3ff00",
      borderColor: "#007052",
      borderWidth: 5,
      borderRadius: 20,
    },
    title: {
      text: "Another Example Chart",
    },
    subtitle: {
      text: "With a subtitle! And styling!",
    },
    series: [series[0], series[1]],
  };

  function toggleThirdSeries() {
    const existingSeries = chart.series.find((s) => s.name === "Group 3");

    if (existingSeries) {
      existingSeries.remove();
      thirdSeriesVisible = false;
    } else {
      chart.addSeries(series[2]);
      thirdSeriesVisible = true;
    }
  }
</script>

<p>The Bronx Innovation</p>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <div class="chart">
        <Chart bind:chart {options} highcharts={Highcharts} />
        <p>Info on data</p>
      </div>
    {/snippet}

    <h2>
      The Bronx is full of potential Leonardos and Einsteins. They're just not
      given the resources to thrive.
    </h2>
    {#snippet scrolly()}
      <p>
        How do poverty and educational inequality in The Bronx limit Black and
        Latino youth from pursuing creative or STEAM degrees? The Bronx is a
        place bursting with creative and scientific potential, but systemically
        underfunded. What if you had the talent to be an innovator but not the
        resources?
      </p>
    {/snippet}
  </Scroller>
</div>

<style>
</style>
