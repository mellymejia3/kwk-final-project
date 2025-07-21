<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
      type: "pie",
    },
    title: {
      text: "Population Rates by Race/Ethnicity",
    },
    plotOptions: {
      pie: {
        allowPointSelect: true,
        dataLabels: [
          {
            enabled: true,
            distance: 20,
          },
          {
            enabled: true,
            distance: -40,
            format: "{point.percentage:.1f}%",
            style: {
              fontSize: "1.2em",
              textOutline: "none",
            },
            filter: {
              operator: ">",
              property: "percentage",
              value: 10,
            },
          },
        ],
      },
    },
    series: [
      {
        name: "Race/Ethnicity",
        data: [
          {
            name: "Black",
            y: 484151,
            sliced: true,
            selected: true,
            color: "#a1261d",
          },
          {
            name: "Hispanic",
            y: 779093,
            color: "#d4d3c1",
          },
          {
            name: "Asian",
            y: 57790,
            color: "#c1d4d3",
          },
          {
            name: "White",
            y: 223793,
            color: "#737373",
          },
        ],
      },
    ],
  };
</script>

<header class="section-header">
  <p>Percent Poverty by Race/Ethnicity</p>
  <div class="divider"></div>
</header>

<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>
        <h3 style= "color: black">The Bronx: Full of Talent, Short on Wealth</h3>
      </ArticleText>

      <ArticleText>
        <p>
          The Bronx is full of diversity, inhabited by residents who come from
          all walks of life.
        </p>
      </ArticleText>

      <ArticleText>
        Black residents make up 30% of the population. While the Hispanic
        community make up 50%.
      </ArticleText>

      <ArticleText>
        According to data from the Black Wealth Data Center, 26.9% of Black
        Bronx residents live below the poverty line.
      </ArticleText>
    {/snippet}
  </Scroller>
</div>

<style>
  .chart {
    width: 90%;
    margin: 0px auto;
  }
</style>
