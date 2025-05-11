---
id: getting-started
title: Getting Started
---

Create React App is an officially supported way to create single-page React
applications. It offers a modern build setup with no configuration.

## Quick Start
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Aprende Verbos Irregulares</title>
  <script src="https://cdn.tailwindcss.com "></script>
</head>
<body class="bg-gradient-to-br from-blue-50 to-indigo-100 min-h-screen">

  <!-- Header -->
  <header class="bg-indigo-700 text-white shadow-lg">
    <div class="container mx-auto px-4 py-6 flex flex-col md:flex-row items-center justify-between">
      <div class="flex items-center mb-4 md:mb-0">
        <svg class="w-10 h-10 mr-3" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M12 2L2 7L12 12L22 7L12 2Z" />
          <path d="M2 17L12 22L22 17" />
          <path d="M2 12L12 17L22 12" />
        </svg>
        <h1 class="text-3xl font-bold">Aprende 120 Verbos Irregulares</h1>
      </div>
      <p class="text-xl italic">En solo dos horas</p>
    </div>
  </header>

  <!-- Navigation Tabs -->
  <nav class="bg-white shadow-md sticky top-0 z-10">
    <div class="container mx-auto px-4">
      <ul class="flex overflow-x-auto space-x-4 py-3">
        <li><button onclick="showTab('overview')" class="tab-btn active">Visión General</button></li>
        <li><button onclick="showTab('verbs')" class="tab-btn">Lista de Verbos</button></li>
        <li><button onclick="showTab('study')" class="tab-btn">Método de Estudio</button></li>
        <li><button onclick="showTab('quiz')" class="tab-btn">Prueba Tú Mismo</button></li>
        <li><button onclick="showTab('flashcards')" class="tab-btn">Tarjetas Interactivas</button></li>
      </ul>
    </div>
  </nav>

  <!-- Main Content -->
  <main class="container mx-auto px-4 py-8">

    <!-- Overview Tab -->
    <section id="overview" class="tab-content max-w-4xl mx-auto">
      <div class="bg-white rounded-lg shadow-lg p-6 mb-8">
        <h2 class="text-2xl font-bold mb-4 text-indigo-700">¿Por qué aprender verbos irregulares?</h2>
        <p class="mb-4">
          Los verbos irregulares son esenciales para construir frases correctas en inglés.
        </p>
        <p class="mb-4">
          Al dominar estos 120 verbos, podrás comunicarte eficazmente en inglés en situaciones cotidianas.
        </p>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mt-6">
          <div class="bg-indigo-50 p-4 rounded-lg text-center">
            <div class="text-4xl font-bold text-indigo-600">90%</div>
            <p class="text-sm text-gray-600">De la comunicación cotidiana</p>
          </div>
          <div class="bg-indigo-50 p-4 rounded-lg text-center">
            <div class="text-4xl font-bold text-indigo-600">2h</div>
            <p class="text-sm text-gray-600">De estudio concentrado</p>
          </div>
          <div class="bg-indigo-50 p-4 rounded-lg text-center">
            <div class="text-4xl font-bold text-indigo-600">120</div>
            <p class="text-sm text-gray-600">Verbos clave aprendidos</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Verbs List Tab -->
    <section id="verbs" class="tab-content hidden max-w-6xl mx-auto">
      <div class="bg-white rounded-lg shadow-lg p-6 mb-6">
        <h2 class="text-2xl font-bold mb-4 text-indigo-700">Lista Completa de Verbos Irregulares</h2>
        <input type="text" id="searchInput" placeholder="Buscar verbo..." class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500 mb-4" />

        <div class="overflow-x-auto">
          <table class="w-full min-w-max table-auto">
            <thead>
              <tr class="bg-indigo-100 text-indigo-800">
                <th class="px-4 py-3 text-left">Infinitivo</th>
                <th class="px-4 py-3 text-left">Pasado Simple</th>
                <th class="px-4 py-3 text-left">Participio Pasado</th>
                <th class="px-4 py-3 text-left">Español</th>
              </tr>
            </thead>
            <tbody id="verbTable" class="divide-y divide-gray-200">
              <!-- Lista de verbos -->
            </tbody>
          </table>
        </div>
      </div>
    </section>

    <!-- Study Method Tab -->
    <section id="study" class="tab-content hidden max-w-4xl mx-auto">
      <div class="bg-white rounded-lg shadow-lg p-6 mb-6">
        <h2 class="text-2xl font-bold mb-4 text-indigo-700">Método Efectivo para Aprender Rápido</h2>
        <div class="space-y-6">
          <div class="bg-indigo-50 p-4 rounded-lg">
            <h3 class="font-bold text-indigo-600 mb-2">Paso 1: Categoriza los Verbos</h3>
            <ul class="list-disc pl-5 text-sm text-gray-700">
              <li><span class="font-semibold">A-B-B</span>: be → was/were → been</li>
              <li><span class="font-semibold">A-A-B</span>: cut → cut → cut</li>
              <li><span class="font-semibold">A-B-C</span>: sing → sang → sung</li>
            </ul>
          </div>
          <div class="bg-indigo-50 p-4 rounded-lg">
            <h3 class="font-bold text-indigo-600 mb-2">Paso 2: Usa Tarjetas de Memoria</h3>
            <p>Haz tarjetas con el infinitivo en un lado y las formas pasadas en el otro.</p>
          </div>
          <div class="bg-indigo-50 p-4 rounded-lg">
            <h3 class="font-bold text-indigo-600 mb-2">Paso 3: Asociaciones Mnemotécnicas</h3>
            <ul class="list-disc pl-5 text-sm text-gray-700">
              <li>"I saw the sun shine brightly"</li>
              <li>"The man ran and his shoes were run out"</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Quiz Tab -->
    <section id="quiz" class="tab-content hidden max-w-4xl mx-auto">
      <div class="bg-white rounded-lg shadow-lg p-6 mb-6">
        <h2 class="text-2xl font-bold mb-4 text-indigo-700">¡Pon a Prueba Tus Conocimientos!</h2>
        <div class="bg-indigo-50 p-4 rounded-lg mb-6">
          <p class="mb-4">Elige la forma correcta del verbo para completar estas oraciones:</p>
          <form id="quizForm">
            <div class="space-y-4">
              <div class="bg-white p-4 rounded shadow">
                <p class="mb-2">1. She ______ her homework yesterday.</p>
                <label class="block"><input type="radio" name="q1" value="did"> did</label>
                <label class="block"><input type="radio" name="q1" value="do"> do</label>
                <label class="block"><input type="radio" name="q1" value="done"> done</label>
              </div>
              <div class="bg-white p-4 rounded shadow">
                <p class="mb-2">2. I have ______ this book twice.</p>
                <label class="block"><input type="radio" name="q2" value="read"> read</label>
                <label class="block"><input type="radio" name="q2" value="reading"> reading</label>
                <label class="block"><input type="radio" name="q2" value="readed"> readed</label>
              </div>
              <button type="submit" class="mt-4 bg-indigo-600 text-white px-6 py-2 rounded hover:bg-indigo-700 transition">Calificar</button>
            </div>
          </form>
          <div id="result" class="mt-4 font-bold text-green-600"></div>
        </div>
      </div>
    </section>

    <!-- Flashcards Tab -->
    <section id="flashcards" class="tab-content hidden max-w-4xl mx-auto">
      <div class="bg-white rounded-lg shadow-lg p-6 mb-6">
        <h2 class="text-2xl font-bold mb-4 text-indigo-700">Tarjetas de Memoria Interactivas</h2>
        <div class="bg-indigo-50 p-6 rounded-lg text-center">
          <div id="flashcard" class="w-full max-w-md mx-auto aspect-[3/2] bg-white rounded-lg shadow-md flex items-center justify-center text-center text-lg font-medium cursor-pointer p-6 transition-all duration-300 transform hover:scale-105" onclick="flipCard()">
            Haz clic para comenzar
          </div>
          <div class="mt-4 space-x-2">
            <button onclick="prevCard()" class="bg-gray-500 text-white px-4 py-2 rounded">Anterior</button>
            <button onclick="nextCard()" class="bg-indigo-600 text-white px-4 py-2 rounded">Siguiente</button>
          </div>
        </div>
      </div>
    </section>

  </main>

  <!-- Footer -->
  <footer class="bg-indigo-700 text-white py-8">
    <div class="container mx-auto px-4 text-center text-sm">
      © 2025 Aprende 120 Verbos Irregulares. Todos los derechos reservados.
    </div>
  </footer>

  <!-- Script -->
  <script>
    const verbs = [
      { base: "be", pastSimple: "was/were", pastParticiple: "been", spanish: "ser/estar" },
      { base: "have", pastSimple: "had", pastParticiple: "had", spanish: "tener" },
      { base: "go", pastSimple: "went", pastParticiple: "gone", spanish: "ir" },
      { base: "do", pastSimple: "did", pastParticiple: "done", spanish: "hacer" },
      { base: "say", pastSimple: "said", pastParticiple: "said", spanish: "decir" },
      { base: "see", pastSimple: "saw", pastParticiple: "seen", spanish: "ver" },
      { base: "take", pastSimple: "took", pastParticiple: "taken", spanish: "tomar" },
      { base: "know", pastSimple: "knew", pastParticiple: "known", spanish: "saber" },
      { base: "get", pastSimple: "got", pastParticiple: "gotten/got", spanish: "obtener" },
      { base: "make", pastSimple: "made", pastParticiple: "made", spanish: "hacer" }
    ];

    let currentCardIndex = 0;
    let cardSide = 'front'; // 'front' or 'back'

    function showTab(tabId) {
      document.querySelectorAll('.tab-content').forEach(el => el.classList.add('hidden'));
      document.getElementById(tabId).classList.remove('hidden');
      document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
      event.currentTarget.classList.add('active');
    }

    // Load verbs into table
    const verbTable = document.getElementById("verbTable");
    verbs.forEach(verb => {
      const row = document.createElement("tr");
      row.innerHTML = `
        <td class="px-4 py-3">${verb.base}</td>
        <td class="px-4 py-3">${verb.pastSimple}</td>
        <td class="px-4 py-3">${verb.pastParticiple}</td>
        <td class="px-4 py-3">${verb.spanish}</td>
      `;
      verbTable.appendChild(row);
    });

    // Search functionality
    document.getElementById("searchInput").addEventListener("input", function () {
      const term = this.value.toLowerCase();
      const rows = verbTable.getElementsByTagName("tr");
      Array.from(rows).forEach(row => {
        const cells = row.getElementsByTagName("td");
        let match = false;
        Array.from(cells).forEach(cell => {
          if (cell.textContent.toLowerCase().includes(term)) match = true;
        });
        row.style.display = match ? "" : "none";
      });
    });

    // Quiz logic
    document.getElementById("quizForm").addEventListener("submit", function (e) {
      e.preventDefault();
      let score = 0;
      if (document.querySelector('input[name="q1"]:checked')?.value === "did") score++;
      if (document.querySelector('input[name="q2"]:checked')?.value === "read") score++;

      document.getElementById("result").textContent = `Tienes ${score} de 2 respuestas correctas.`;
    });

    // Flashcards logic
    const flashcard = document.getElementById("flashcard");

    function updateCard() {
      if (verbs.length === 0) return;
      const verb = verbs[currentCardIndex];
      if (cardSide === 'front') {
        flashcard.textContent = `Verbo: ${verb.base}`;
        flashcard.className = 'bg-white';
      } else {
        flashcard.textContent = `Past: ${verb.pastSimple} | Participio: ${verb.pastParticiple} | Español: ${verb.spanish}`;
        flashcard.className = 'bg-indigo-100';
      }
    }

    function flipCard() {
      cardSide = cardSide === 'front' ? 'back' : 'front';
      updateCard();
    }

    function nextCard() {
      currentCardIndex = (currentCardIndex + 1) % verbs.length;
      cardSide = 'front';
      updateCard();
    }

    function prevCard() {
      currentCardIndex = (currentCardIndex - 1 + verbs.length) % verbs.length;
      cardSide = 'front';
      updateCard();
    }

    // Initialize first card
    updateCard();
  </script>
</body>
</html>
```sh
npx create-react-app my-app
cd my-app
npm start
```

> If you've previously installed `create-react-app` globally via `npm install -g create-react-app`, we recommend you uninstall the package using `npm uninstall -g create-react-app` or `yarn global remove create-react-app` to ensure that `npx` always uses the latest version.

_([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) comes with npm 5.2+ and higher, see [instructions for older npm versions](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))_

Then open [http://localhost:3000/](http://localhost:3000/) to see your app.

When you’re ready to deploy to production, create a minified bundle with `npm run build`.

<p align='center'>
<img src='https://cdn.jsdelivr.net/gh/facebook/create-react-app@27b42ac7efa018f2541153ab30d63180f5fa39e0/screencast.svg' width='600' alt='npm start' />
</p>

### Get Started Immediately

You **don’t** need to install or configure tools like webpack or Babel. They are preconfigured and hidden so that you can focus on the code.

Create a project, and you’re good to go.

## Creating an App

**You’ll need to have Node >= 14 on your local development machine** (but it’s not required on the server). You can use [nvm](https://github.com/creationix/nvm#installation) (macOS/Linux) or [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) to switch Node versions between different projects.

To create a new app, you may choose one of the following methods:

### npx

```sh
npx create-react-app@latest my-app
```

_([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) comes with npm 5.2+ and higher, see [instructions for older npm versions](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))_

### npm

```sh
npm init react-app my-app
```

_`npm init <initializer>` is available in npm 6+_

### Yarn

```sh
yarn create react-app my-app
```

_`yarn create` is available in Yarn 0.25+_

### Selecting a template

You can now optionally start a new app from a template by appending `--template [template-name]` to the creation command.

If you don't select a template, we'll create your project with our base template.

Templates are always named in the format `cra-template-[template-name]`, however you only need to provide the `[template-name]` to the creation command.

```sh
npx create-react-app my-app --template [template-name]
```

> You can find a list of available templates by searching for ["cra-template-\*"](https://www.npmjs.com/search?q=cra-template-*) on npm.

Our [Custom Templates](custom-templates.md) documentation describes how you can build your own template.

#### Creating a TypeScript app

You can start a new TypeScript app using templates. To use our provided TypeScript template, append `--template typescript` to the creation command.

```sh
npx create-react-app my-app --template typescript
```

If you already have a project and would like to add TypeScript, see our [Adding TypeScript](adding-typescript.md) documentation.

### Selecting a package manager

When you create a new app, the CLI will use [npm](https://docs.npmjs.com) or [Yarn](https://yarnpkg.com/) to install dependencies, depending on which tool you use to run `create-react-app`. For example:

```sh
# Run this to use npm
npx create-react-app my-app
# Or run this to use yarn
yarn create react-app my-app
```

## Output

Running any of these commands will create a directory called `my-app` inside the current folder. Inside that directory, it will generate the initial project structure and install the transitive dependencies:

```
my-app
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── public
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
└── src
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── index.css
    ├── index.js
    ├── logo.svg
    ├── serviceWorker.js
    └── setupTests.js
```

No configuration or complicated folder structures, only the files you need to build your app. Once the installation is done, you can open your project folder:

```sh
cd my-app
```

## Scripts

Inside the newly created project, you can run some built-in commands:

### `npm start` or `yarn start`

Runs the app in development mode. Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will automatically reload if you make changes to the code. You will see the build errors and lint warnings in the console.

<p align='center'>
<img src='https://cdn.jsdelivr.net/gh/marionebl/create-react-app@9f6282671c54f0874afd37a72f6689727b562498/screencast-error.svg' width='600' alt='Build errors' />
</p>

### `npm test` or `yarn test`

Runs the test watcher in an interactive mode. By default, runs tests related to files changed since the last commit.

[Read more about testing](running-tests.md).

### `npm run build` or `yarn build`

Builds the app for production to the `build` folder. It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.

Your app is ready to be deployed.
