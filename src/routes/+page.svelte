<script>
</script>

<main>
  <header>
    <h1>Geburtstagsfestival</h1>
  </header>

  <div class="menucontent">
    <div class="menupoint">
      <h2>Infos</h2>
      <p>Geburtstag Hannes: 10.11</p>
      <p>Geburtstag Lene: 11.11</p>

      <p>Einlass: 8.10 18 Uhr</p>
    </div>
    <div class="menupoint">
      <h2>Programm</h2>
      <p>Das Programm wird in Kürze bekannt gegeben.</p>
      <h3>Freitag, 8.11</h3>
      <h3>Samstag, 9.11</h3>
      <h3>Sonntag, 10.11</h3>
      <h3>Montag, 11.11</h3>
      <p>Fahrt nach hause und kommt mal klar ey</p>
    </div>
    <div class="menupoint">
      <h2>Location</h2>
      <p>Adresse</p>
    </div>
    <div class="menupoint">
      <h2>Magic Hour</h2>
      <p>hmm simsalabim</p>
    </div>
  </div>
</main>

<style>
  :global(body) {
    color: white;
    background-color: #342434;
    background: linear-gradient(180deg, #342434 40%, #541e54 100%);
    word-wrap: break-word;
  }

  * {
    margin: 0;
    padding: 0;
  }
  header {
    /* The image used */
    background-image: url("../assets/castle.webp");

    /* Full height */
    /* Create the parallax scrolling effect */
    background-position: center;
    background-repeat: no-repeat;
    background-size: contain;
    height: 100vw;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
  }

  :global(h1) {
    color: white;
    font-size: 25px;
    text-shadow: 7px 5px 15px #000000;
    font-family: SundayFont;
    margin: 0 auto;
  }

  .container {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
  }

  h2 {
    font-size: 20px;
    padding-bottom: 7px;
    margin: 0 auto;
    color: #fab45c;
    font-family: SundayFont;
  }

  main {
    height: 100%;
    width: 100%;
  }

  .menucontent {
    display: flex;
    flex-direction: column;
    gap: 30px;
    padding: 20px;
  }
  .menupoint {
    border-bottom: 1px solid #9948b2;
    padding-bottom: 20px;
  }

  @font-face {
    font-family: SundayFont;
    src: url(../assets/OTF/Sunday-Regular.otf);
  }
</style>
