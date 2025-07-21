<script>
  let { children } = $props();
</script>

<div class="article-text">
  <p>
    {@render children()}
  </p>
</div>

<style>
  .article-text {
    margin: 50vh auto;
    width: 50%;
    background-color: #f8f5ed;
    color: Black;
    border: solid #a1261d 3px;
    border-radius: 20px;
    padding: 20px;
    box-shadow: 16px 16px #737373;
  }
</style>
