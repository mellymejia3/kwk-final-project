<script>
  let { heading, title, picture, headline, subtitle } = $props();
</script>

<div class="heading">
  <p>{heading}</p>
  <h1>{title}</h1>
</div>

<img src={picture} alt="headline" width="700" height="250" />
<div>
  <h2>{headline}</h2>
  <h3>{subtitle}</h3>
</div>

<style>
  .heading {
    padding: 2px;
    position: relative;
    top: -150px;
    align-items: center;
    text-align: center;
  }

  /*.title-card {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .content {
    max-width: 700px;
    background-color: #ebebeb;
    padding: 2rem;
    border: 6px solid #2e2e2e;
    border-radius: 2rem;
    box-shadow: 16px 16px #808583;
  } not being used for now*/

  h1 {
    font-family: "Playfair Display";
    font-size: 56pt;
    margin: 0;
    color: #40382d;
  }

  h2 {
    font-family: "Playfair Display";
    font-size: 32pt;
    color: Black;
  }

  h3 {
    font-family: "EB Garamond";
    font-size: 24pt;
    color: #737373;
  }

  p {
    font-family: "EB Garamond";
    font-size: 14pt;
    color: #737373;
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
