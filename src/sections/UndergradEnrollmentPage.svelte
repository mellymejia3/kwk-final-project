<script>
  import * as Highcharts from "highcharts";
  import "highcharts/modules/exporting";
  import { Chart } from "@highcharts/svelte";
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
</script>

<header class="section-header">
  <p>The Cost of Curiosity</p>
  <div class="divider"></div>
</header>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <div class="chart">
        <h1 style= "color: #a1261d">1.6%</h1>
      </div>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText
        >What happens when students like Kayla want to pursue higher education?</ArticleText
      >

      <ArticleText
        >On a national level, only 1.6% of Black youth are enrolled in undergraduate programs — a decrease from 1.9% reported in the 2016 census.</ArticleText
      >
      <ArticleText
        >Application fees and tuition, along with the cost of art supplies and
        technology, quickly add up for students pursuing higher education. These
        are expenses that students like Kayla often can’t afford on their own.
        Without access to proper resources and support systems, it becomes harder to enroll in college.</ArticleText
      >
      <ArticleText
        >Creativity isn’t just about talent—it’s about access. And right now,
        the cost of entry is too high for many Bronx youth.</ArticleText
      >
    {/snippet}
  </Scroller>
</div>

<style>
</style>
