<script>
  import Scroller from "../lib/Scroller.svelte";
  import ArticleText from "../lib/ArticleText.svelte";
</script>

<p>The Bronx Innovation</p>

<div>
  <Scroller layout="left">
    {#snippet sticky()}
      <img class="duck-img" src="duck.png" alt="KWK rubber duck!" />
    {/snippet}

    <h2>
      The Bronx is full of potential Leonardos and Einsteins. They're just not
      given the resources to thrive.
    </h2>
    {#snippet scrolly()}
      <ArticleText>
        <p>
          How do poverty and educational inequality in The Bronx limit Black and
          Latino youth from pursuing creative or STEAM degrees? The Bronx is a
          place bursting with creative and scientific potential, but
          systemically underfunded. What if you had the talent to be an
          innovator but not the resources?
        </p>
      </ArticleText>
    {/snippet}
  </Scroller>
</div>

<style>
</style>
