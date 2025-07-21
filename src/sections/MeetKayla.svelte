<script>
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
</script>

<header class="section-header">
  <p>Meet Kayla</p>
  <div class="divider"></div>
</header>

<div>
  <Scroller layout="right">
    {#snippet sticky()}
      <div class="image-column">
        <img src="kayla.png" alt="Portrait of Kayla" />
      </div>
      <blockquote>
        "I want to be an engineer, but my school cut the robotics club last
        year."
      </blockquote>
    {/snippet}

    {#snippet scrolly()}
      <ArticleText>
        <strong>Meet Kayla! </strong>
      </ArticleText>

      <ArticleText>
        Kayla is a straight-A student at a public school in the Bronx.
      </ArticleText>

      <ArticleText>
        She is a first-generation American, and her school has a 30:1
        student-teacher ratio.
      </ArticleText>

      <ArticleText>
        <strong>
          She hope's to go to college for enginerring. Lets see what her options
          are.
        </strong>
      </ArticleText>
    {/snippet}
  </Scroller>
</div>

<style>
</style>
