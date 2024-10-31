<script>
  import { Confetti } from "svelte-confetti";
  import ToggleConfetti from "./ToggleConfetti.svelte";
  let showModal = false;

  function handleSubmit(event) {
    event.preventDefault();
    const input = document.querySelector("#riddle-input").value;
    if (input === "Bierbaum") {
      showModal = true;
    } else {
      alert("Incorrect. Try again.");
    }
  }
</script>

<div class="content">
  <div class="infos">
    <span>Hannes - 10.11 </span>
    <a
      href="https://www.google.de/maps/place/Herrenhaus+L%C3%BCbbenow/@53.4504705,13.8041292,17z/data=!3m1!4b1!4m6!3m5!1s0x47aa2e2d960c64b5:0xf0727042acd00c43!8m2!3d53.4504705!4d13.8067041!16s%2Fg%2F11c6_vkyw8?entry=ttu&g_ep=EgoyMDI0MTAyMy4wIKXMDSoASAFQAw%3D%3D"
      target="_blank">Herrenhaus bei Lübbenow</a
    ><span>Lene - 11.11</span>
  </div>

  <ToggleConfetti>
    <button class="button" slot="label">Drück mich</button>
    <div
      style="top: -50px; left: 0; height: 100vh; width: 110vw; justify-content: center;"
    >
      <Confetti
        x={[-5, 5]}
        y={[0.5, 0.5]}
        delay={[500, 2000]}
        infinite
        duration="8000"
        amount="400"
        fallDistance="100vh"
        size="50"
        colorArray={[
          "url(./images/hannes.png)",
          "url(./images/lene.png)",
          "url(./images/lene_eichhorn.png)",
          "url(./images/hanne_schild.png)",
        ]}
      />
    </div>
  </ToggleConfetti>

  <div class="introduction">
    Es war einmal ein geheimnisvolles Herrenhaus, versteckt in den endlosen
    Weiten von Lübbenow, das nur darauf wartete, zum Schauplatz eines
    märchenhaften Festes zu werden. Anlässlich des Ehrentages unserer geliebten
    Geburtstagskinder Lene und Hannes versammeln sich Freunde von nah und fern,
    um ein Wochenende voller Glitzer, Lachen und Magie zu erleben. Dort,
    inmitten von Sauna, Pool und weiten Hallen, haben wir Platz für all unsere
    wilden Träume und Geschichten. Packt eure funkelnden Festivalgewänder, eure
    mutigsten Tanzschritte und die schönsten Anekdoten über die beiden ein –
    denn hier feiern wir ein Fest, das selbst den Sternen noch lange in
    Erinnerung bleiben wird!
  </div>
  <div class="menucontent">
    <span class="divider"></span>
    <div class="menupoint">
      <h2>Tribute von Lübbenow</h2>
      <div class="eventdescription">
        Über den weiten Hallen von Lübbenow erhebt sich ein Fest voller Magie
        und Tradition, bereit, das wildeste Turnier des Jahres zu beherbergen.
        Teams aus nah und fern treten in außergewöhnlichen Disziplinen an, um
        für Lene und Hannes um den Sieg zu kämpfen. Ob beim Staffelsaufen, wo
        Ausdauer und Teamgeist gefragt sind, in der verrückten Quizshow, die
        Wissen und Schnelligkeit fordert, oder bei der legendären Reise ins
        Delirium.
        <br />
        Also, schnappt euch eure funkelnden Gewänder, bringt euren Kampfgeist mit
        und bereitet euch darauf vor, Seite an Seite zu triumphieren und zu feiern.
        Ein Spektakel für die Ewigkeit.
      </div>
      <h3>Freitag, 8.11</h3>
      <p class="competition">
        <strong>21:30 Uhr:</strong> Geschichten aus der Kindheit
      </p>
      <p class="competition"><strong>22:00 Uhr:</strong> What is it?</p>
      <h3>Samstag, 9.11</h3>
      <p class="competition"><strong>13:00 Uhr:</strong> Staffelsaufen</p>
      <p class="competition"><strong>14:00 Uhr:</strong> Pfeffi Pirsch</p>
      <p class="competition"><strong>18:00 Uhr:</strong> Reise ins Delirium</p>
      <p class="competition"><strong>18:30 Uhr:</strong> Quizshow</p>
      <p class="competition"><strong>19:00 Uhr:</strong> Siegerehrung</p>
    </div>
    <span class="divider"></span>
    <div class="menupoint">
      <h2>Rätsel</h2>
      <h3 class="riddle">
        Ich bin nie dicht, doch alle in mir sind es ständig.
      </h3>
      <p class="riddle-text">Was bin ich?</p>
      <form on:submit={handleSubmit}>
        <input type="text" id="riddle-input" placeholder="Deine Antwort" />
        <button class="button" type="submit">ich hab's</button>
      </form>

      {#if showModal}
        <div class="modal">
          <div class="modal-content">
            <p class="riddle-text">
              Herzlichen Glückwunsch! Du hast das Rätsel gelöst.
            </p>
            <video width="320" height="240" controls>
              <source src="images/hannesvideo.MP4" type="video/mp4" />
              Your browser does not support the video tag.
            </video>
          </div>
        </div>
      {/if}
    </div>

    <span class="divider"></span>
    <div class="menupoint">
      <h2>Line Up</h2>
      <h3>Freitag, 8.11</h3>
      <p><strong>Ab 16 Uhr:</strong> Einlass</p>
      <h3>Samstag, 9.11</h3>
      <p class="party" href="#party"><strong>20:00 Uhr:</strong> DJ Paquet</p>
      <p class="party" href="#party"><strong>22:00 Uhr:</strong> DJ Tomasch</p>
      <h3>Sonntag, 10.11</h3>
      <p><strong>Hannes Geburtstag</strong></p>
      <p class="party" href="#party"><strong>02:00 Uhr:</strong> DJ Heggi</p>
      <p class="party" href="#party"><strong>00:00 Uhr:</strong> DJ AHAB</p>
      <h3>Montag, 11.11</h3>
      <p><strong>Lene Geburtstag</strong></p>
      <p><strong>10:00 Uhr:</strong> Bitte fahrt nach hause und kommt klar</p>
    </div>
    <span class="divider"></span>
    <div class="menupoint">
      <h2>Magic Hour</h2>
      <p>
        <a
          class="button"
          href="https://photos.app.goo.gl/q9oTrQJNLcgsKnEm8"
          target="_blank">hmm simsalabim</a
        >
      </p>
    </div>
    <span class="divider"></span>
    <div class="menupoint">
      <h2>Location</h2>
      <p>
        <a
          href="https://www.google.de/maps/place/Herrenhaus+L%C3%BCbbenow/@53.4504705,13.8041292,17z/data=!3m1!4b1!4m6!3m5!1s0x47aa2e2d960c64b5:0xf0727042acd00c43!8m2!3d53.4504705!4d13.8067041!16s%2Fg%2F11c6_vkyw8?entry=ttu&g_ep=EgoyMDI0MTAyMy4wIKXMDSoASAFQAw%3D%3D"
          target="_blank">Herrenhaus Lübbenow</a
        >
      </p>
      <p>Dorfstraße 2, 17337 Uckerland</p>
    </div>
  </div>
</div>

<style>
  .riddle-text {
    font-family: Arial, Helvetica, sans-serif;
  }
  input {
    padding: 15px;
    border-radius: 5px;
    border: none;
    margin: 20px 0;
    width: 90%;
    font-size: 16px;
  }
  .riddle {
    color: white;
    line-height: 1.5;
  }
  .riddle h3 {
    margin-bottom: 20px;
  }
  .eventdescription {
    line-height: 1.5;
    font-size: 14px;
    opacity: 0.7;
    text-transform: uppercase;
    color: white;
  }
  .button {
    background-color: #c43e88;
    color: #fcf1d9;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    font-size: 16px;
    font-family: SundayFont;
    cursor: pointer;
    margin: 0 auto;
    z-index: 1;
    margin-bottom: 50px;
  }
  .divider {
    display: flex;
    width: 30%;
    background-color: #382236;
    height: 1px;
    align-self: center;
  }
  header {
    text-shadow: 7px 5px 15px #000000;
  }

  h3 {
    margin-top: 10px;
    font-size: 16px;
    font-family: SundayFont;
  }

  .infos {
    display: flex;
    text-transform: uppercase;
    justify-content: space-between;
    font-size: 10px;
    text-align: center;
    padding: 30px 10px;
    font-family: SundayFont;

    > * {
      color: #fcf1d9;
    }
  }

  strong {
    margin-top: -4px;
    color: #fcf1d9;
  }

  .content {
    background: linear-gradient(180deg, #32213a 0%, #812658 100%);
  }

  .introduction {
    font-size: 15px;
    line-height: 1.5;
    opacity: 0.7;
    text-transform: uppercase;
    text-align: center;
    margin: 0 20px 30px;
    color: white;
  }

  .menucontent {
    display: flex;
    flex-direction: column;
    gap: 50px;
    text-align: center;
    padding-top: 30px;
    padding-bottom: 100px;
  }

  .menupoint {
    margin: 0 20px;
    text-align: left;
  }

  .menupoint p {
    margin-bottom: 15px;
  }
</style>
