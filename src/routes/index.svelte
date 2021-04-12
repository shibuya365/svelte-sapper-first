<script>
</script>

<svelte:head>
  <title>Sapper first App</title>
</svelte:head>

<div>
  <img src="no-text-logo.png" alt="" />
  <h1>Hello</h1>
  <p>Find your contents</p>
  <a href="jobs" class="btn">Vew</a>
</div>

<style>
  h1,
  p {
    text-align: center;
    margin: 0 auto;
  }
  h1 {
    font-size: 2em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }
  img {
    width: 200px;
    margin: 0 auto;
    display: block;
  }
  a {
    margin-top: 40px;
  }
  div {
    margin-top: 60px;
    text-align: center;
  }
  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
  :global(.btn) {
    display: inline-block;
    background: #ff3e00;
    color: white;
    padding: 10px 15px;
    text-decoration: none;
    border-radius: 8px;
    text-transform: uppercase;
    font-size: 11px;
    letter-spacing: 1px;
    font-weight: 600;
    border: 0;
    /* font-family: 'Quicksand'; */
  }
</style>
