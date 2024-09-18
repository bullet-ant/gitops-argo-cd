<script>
  import "./app.css";
  import pkg from "../package.json";

  let src =
    "https://media.tenor.com/MnCp90aKFAkAAAAM/white-cat-eating-salad.gif";
</script>

<main>
  <img {src} alt="a legendary meme" />
  <h1>v{pkg.version}</h1>
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    min-height: 90vh;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
  }
</style>
