# Meine_erste_website

<!doctype html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Über mich lol | Tara</title>

  <style>
    * {
      box-sizing: border-box;
    }

    :root {
      --bg: rgb(15,23,42);
      --text: rgb(248,250,252);
      --accent: rgb(96,165,250);
      --nav: rgb(147,197,253);
      --card: rgb(30,41,59);
      --border: rgb(51,65,85);
    }

    body {
      margin: 0;
      padding: 40px 20px;
      background: var(--bg);
      color: var(--text);
      font-family: Arial, sans-serif;
      transition: background 0.4s, color 0.4s;
    }

    .container {
      max-width: 900px;
      margin: auto;
    }

    nav {
      color: var(--nav);
      letter-spacing: 3px;
      font-size: 12px;
      margin-bottom: 50px;
    }

    .hero {
      display: flex;
      align-items: center;
      gap: 40px;
    }

    .intro {
      flex: 1;
    }

    .tag {
      color: var(--accent);
      letter-spacing: 3px;
      font-size: 13px;
    }

    h1 {
      font-size: clamp(48px, 10vw, 90px);
      margin: 10px 0;
    }

    h2 {
      color: var(--accent);
    }

    .intro p {
      color: var(--text);
      line-height: 1.8;
    }

    a {
      color: var(--accent);
      transition: color 0.3s;
    }

    .photo {
      width: 42%;
      max-width: 320px;
      height: 380px;
      object-fit: cover;
      border-radius: 18px;
      border: 1px solid var(--border);
    }

    .about {
      margin-top: 60px;
      padding: 28px;
      background: var(--card);
      border-radius: 18px;
      transition: background 0.4s;
    }

    .about p {
      color: var(--text);
      line-height: 1.8;
    }

    .blue {
      color: var(--accent);
    }

    /* INTERACTIVE SECTIONS */

    .interactive-area {
      margin-top: 30px;
      padding: 28px;
      background: var(--card);
      border-radius: 18px;
      text-align: center;
      transition: background 0.4s;
    }

    .interactive-area h2 {
      color: var(--accent);
    }

    .interactive-area p {
      line-height: 1.7;
    }

    .interactive-area button {
      padding: 13px 24px;
      margin: 10px 6px;
      border: none;
      border-radius: 9px;
      background: var(--accent);
      color: var(--bg);
      font-size: 14px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
    }

    .interactive-area button:hover {
      filter: brightness(1.12);
    }

    #noButton {
      position: relative;
    }

    #answer {
      color: var(--accent);
      font-weight: bold;
      min-height: 25px;
    }

    @media (max-width: 600px) {
      body {
        padding: 25px 18px;
      }

      .hero {
        flex-direction: column-reverse;
        align-items: stretch;
        gap: 20px;
      }

      .photo {
        width: 100%;
        max-width: none;
        height: 300px;
      }

      .about {
        margin-top: 35px;
      }
    }
  </style>
</head>

<body>
  <main class="container">

    <nav>MEINE ERSTE WEBSITE</nav>

    <section class="hero">
      <div class="intro">

        <span class="tag">HEY lol, ich bin</span>
        <h1>TARA<span class="blue">.</span></h1>

        <p>
          Hallooo Ich heiße Tara und ich wohne
          <a href="https://www.google.com/">nähe Stuttgart</a>.
        </p>

        <p>
          Ich mag <a href="https://de.wikipedia.org/wiki/Blau">Blau</a>.
          Blau ist sehr schön.
        </p>

        <p>
          Ich höre mega gern Musik. ja.
          Ich mag auch Katzen.
        </p>

        <p>
          Und <a href="https://de.wikipedia.org/wiki/Pink_(Farbe)">Blau</a>.
        </p>

        <p>hahaha</p>

        <p>Naja ist ja auch egal.</p>

      </div>

      <img
        class="photo"
        src="images.jfif"
        alt="Foto von Tara"
      >
    </section>

    <section class="about">

      <h2>
        Ein bisschen mehr ungefragte Details über mich<span class="blue">.</span>
      </h2>

      <p>
        ähm, klären wir mal das Offensichtlichste vorab:
        Meine Lieblingsfarbe ist Blau. Hab ich das schon erwähnt?
        Keine Ahnung. Is auch völlig uninteressant.
      </p>

      <p>
        Wenn ich erwachsen bin, möchte ich, anders als bailey,
        nicht Agility-Sport treiben.
        Gesund sein reicht mir völlig aus.
        Und 7 Katzen wären auch schön, aber muss nicht sein.
      </p>

      <p>
        <a href="https://de.wikipedia.org/wiki/Drachenlord">Ich</a>
        fahre gern Motorrad.
        Aber Ich fahr nicht gerne Motorrad, weil's cool ist.
        Ich fahr Motorrad, weil ich das gerne fahr.
        Abgesehen davon fahr ich gar kein Motorrad.
      </p>

    </section>


    <!-- BUTTON 1: BLUE THEME CHANGER -->

    <section class="interactive-area">

      <h2>Change my vibe.</h2>

      <p>
        Feeling blue? Change the colors of my website.
      </p>

      <button onclick="changeTheme()">
        CHANGE THEME
      </button>

      <p id="themeName">Theme: Midnight Blue</p>

    </section>


    <!-- BUTTON 2: 15 POINTS QUESTION -->

    <section class="interactive-area">

      <h2>Is my website worth 15 points?</h2>

      <p>
        Be honest. Does this website deserve a 15?
      </p>

      <button onclick="yesAnswer()">
        YES
      </button>

      <button id="noButton" onclick="noAnswer()">
        NO
      </button>

      <p id="answer"></p>

    </section>

  </main>


  <script>

    // BLUE THEME CHANGER

    const themes = [
      {
        name: "Midnight Blue",
        bg: "#0f172a",
        text: "#f8fafc",
        accent: "#60a5fa",
        nav: "#93c5fd",
        card: "#1e293b",
        border: "#334155"
      },

      {
        name: "Ocean Blue",
        bg: "#102b46",
        text: "#e0f2fe",
        accent: "#38bdf8",
        nav: "#7dd3fc",
        card: "#164e63",
        border: "#155e75"
      },

      {
        name: "Deep Navy",
        bg: "#172554",
        text: "#dbeafe",
        accent: "#818cf8",
        nav: "#bfdbfe",
        card: "#1e3a8a",
        border: "#3730a3"
      },

      {
        name: "Dark Cyan",
        bg: "#164e63",
        text: "#cffafe",
        accent: "#22d3ee",
        nav: "#a5f3fc",
        card: "#155e75",
        border: "#0e7490"
      }
    ];

    let currentTheme = 0;

    function changeTheme() {

      currentTheme = (currentTheme + 1) % themes.length;

      const theme = themes[currentTheme];

      document.documentElement.style.setProperty("--bg", theme.bg);
      document.documentElement.style.setProperty("--text", theme.text);
      document.documentElement.style.setProperty("--accent", theme.accent);
      document.documentElement.style.setProperty("--nav", theme.nav);
      document.documentElement.style.setProperty("--card", theme.card);
      document.documentElement.style.setProperty("--border", theme.border);

      document.getElementById("themeName").textContent =
        "Theme: " + theme.name;
    }


    // YES BUTTON

    function yesAnswer() {

      document.getElementById("answer").textContent =
        "THANK YOU. I KNEW IT. 15 POINTS IT IS. ★";

    }


    // NO BUTTON

    let noClicks = 0;

    function noAnswer() {

      noClicks++;

      const button = document.getElementById("noButton");

      if (noClicks >= 5) {

        button.style.display = "none";

        document.getElementById("answer").textContent =
          "THE NO BUTTON HAS LEFT THE CHAT. 💀";

        return;
      }

      const x = Math.random() * 120 - 60;
      const y = Math.random() * 60 - 30;

      const scale = 1 - noClicks * 0.12;

      button.style.transform =
        `translate(${x}px, ${y}px) scale(${scale})`;

    }

  </script>

</body>
</html>
