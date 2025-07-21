<script>
  let { heading, title, picture, headline, subtitle } = $props();
</script>

<div class="newspaper-container">
  <p>{heading}</p>
  <h1>{title}</h1>
  <hr class="divider" />

  <div class="headline-image">
    <img src={picture} alt="Bronx Innovation Feature" />
  </div>

  <div>
    <h2>{headline}</h2>
    <p>{subtitle}</p>
  </div>
</div>

<style>
  .headline-image {
    width: 100%;
    max-height: 400px;
    overflow: hidden;
    margin-bottom: 2rem;
    border: 1px solid #a1261d;
    justify-content: center;
    align-items: center;
  }

  .headline-image img {
    width: 100%;
    height: auto;
    display: block;
    object-fit: cover;
  }

  .divider {
    border: none;
    height: 2px;
    background-color: #ddd;
    margin: 1rem auto 2rem auto;
    width: 90%;
  }

  .newspaper-container {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem 1rem;
    text-align: center;
  }

  h1 {
    font-family: "Playfair Display";
    font-size: 56pt;
    margin: 0;
    color: #40382d;
    font-weight: 700;
    margin: 0;
  }

  h2 {
    font-family: "Playfair Display";
    font-size: 32pt;
    font-weight: 700;
    color: Black;
    margin: 0.5rem 0;
  }

  p {
    font-family: "EB Garamond";
    font-size: 14pt;
    color: #737373;
    margin-bottom: 0.5rem;
  }

  @media (max-width: 600px) {
    h1 {
      font-size: 2.2rem;
    }

    p {
      font-size: 1.1rem;
    }
  }
</style>
