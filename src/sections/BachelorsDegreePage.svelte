<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";

  let options = {
    chart: {
      type: "column",
    },
    title: {
      text: "Rate of Bachelors Degree or Higher Attainment, Race/Ethnicity",
    },
    subtitle: {
      text:
        "Source: <a Black Wealth Data Center " +
        'href="https://blackwealthdata.org/explore/education">Black Wealth Data Center</a>',
    },
    xAxis: {
      categories: ["Black", "Hispanic", "White", "Asian"],
      crosshair: true,
      accessibility: {
        description: "Race/Ethnicity",
      },
    },
    yAxis: {
      min: 0,
      title: {
        text: "Percentage",
      },
    },
    plotOptions: {
      column: {
        pointPadding: 0.2,
        borderWidth: 0,
        color: "#a1261d",
      },
    },
    series: [
      {
        name: "",
        data: [38.4, 23, 30.9, 15.7],
      },
    ],
  };
</script>

<header class="section-header">
  <p>The Education Gap</p>
  <div class="divider"></div>
</header>

<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div class="chart">
        <Chart {options} highcharts={Highcharts} />
      </div>
    {/snippet}

    <h2>Bachelor's Degree</h2>
    {#snippet scrolly()}
      <ArticleText>
        Kayla dreams of becoming an engineer. She’s applied to multiple schools
        and earned top grades in high school, even without access to robotics or
        AP STEM courses.
      </ArticleText>
      <ArticleText>
        However, the lack of resources and support has made her journey
        challenging.
      </ArticleText>
      <ArticleText
        >The data shows that many students like Kayla, especially Black and
        Latino youth in The Bronx, are far less likely to complete a bachelor’s
        degree.</ArticleText
      >
    {/snippet}
  </Scroller>
</div>

<style>
  .section-header {
    text-align: left;
    margin: 3rem auto 2rem;
    padding: 0 1rem;
  }

  .section-header .divider {
    height: 2px;
    background-color: #ddd;
    width: 100%;
    max-width: 100%;
  }
</style>
