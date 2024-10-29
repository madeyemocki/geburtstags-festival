<div class="wrapper">
  <div class="wrapper-parallax">
    <div class="background"></div>
    <img
      src="https://i.postimg.cc/rzx8fKyY/pngfind-com-bike-smoke-png-1458660.png"
      class="foreground"
    />
    <h1 class="title">Geburtstagsfestival</h1>
  </div>

  <div class="infos">
    <span>Hannes - 10.11 </span> <span>Herrenhaus bei Lübbenow</span><span
      >Lene - 11.11</span
    >
  </div>
</div>

<style>
  body {
    margin: 0;
  }
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
    height: 70%;
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
    transform: translateZ(-5px) scale(2.045);
  }

  .background,
  .foreground {
    position: absolute;
    height: 100%;
    width: 100%;
    object-fit: cover;
    z-index: -1;
  }

  .title span {
    text-decoration-line: underline;
    text-decoration-style: "solid";
    text-decoration-color: rgb(0 254 238);
    text-decoration-thickness: 5px;
  }

  .infos {
    font-size: 1.2rem;
    padding: 2rem;
    background-color: #333;
    color: white;
    height: 400px;
  }
</style>
