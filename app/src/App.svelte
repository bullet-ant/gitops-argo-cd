<script>
  import "./app.css";
  import pkg from "../package.json";

  let src =
    "https://i.pinimg.com/736x/df/cf/3f/dfcf3f48ab61f0ed8857676a441859dc--doge-meme-doge-dog.jpg";
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
