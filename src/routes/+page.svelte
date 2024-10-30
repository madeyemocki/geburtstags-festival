<script>
  import "../lib/styles.css";
  import Content from "./Content.svelte";
</script>

<main>
  <div class="wrapper">
    <div class="wrapper-parallax">
      <div class="background"></div>
      <img
        src="https://i.postimg.cc/rzx8fKyY/pngfind-com-bike-smoke-png-1458660.png"
        class="foreground"
      />
      <div class="title">
        <h1>Geburtstagsfestival</h1>
        <h1>8.11 - 11.11</h1>
      </div>
    </div>

    <Content></Content>
  </div>
</main>

<style>
  .wrapper {
    height: 100vh;
    overflow-y: auto;
    overflow-x: hidden;
    perspective: 10px;
  }

  .wrapper-parallax {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    transform-style: preserve-3d;
    z-index: -1;
  }

  .background {
    transform: translateZ(-10px) scale(3);
    opacity: 0.8;
    background-image: url("../assets/castle.webp");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    height: 100vh;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
  }

  .foreground {
    transform: translateZ(-10px) scale(2.045);
  }
  .background,
  .foreground {
    position: absolute;
    height: 100%;
    width: 100%;
    object-fit: cover;
    z-index: -1;
  }

  .title {
    display: flex;
    flex-direction: column;
    color: #fcf1d9;
    gap: 20px;
    margin-top: -60px;
  }
</style>
