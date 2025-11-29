<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <title>Inventaire Pause Burger</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <style>
    :root {
      --bg: #111111;
      --card: #1f1f1f;
      --accent: #ff7a00;
      --text: #ffffff;
      --muted: #aaaaaa;
    }
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
        sans-serif;
      background: var(--bg);
      color: var(--text);
    }
    header {
      padding: 10px 16px 6px;
      display: flex;
      align-items: center;
      gap: 10px;
      background: #000;
      border-bottom: 2px solid var(--accent);
    }
    header img {
      height: 42px;
      width: auto;
      border-radius: 6px;
    }
    header .title-block {
      display: flex;
      flex-direction: column;
    }
    header .title {
      font-size: 18px;
      font-weight: 700;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--accent);
    }
    header .subtitle {
      font-size: 11px;
      color: var(--muted);
    }
    .toolbar {
      padding: 8px 12px;
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      background: #181818;
      border-bottom: 1px solid #222;
    }
    button {
      border: none;
      border-radius: 6px;
      padding: 7px 10px;
      font-size: 12px;
      font-weight: 600;
      background: var(--accent);
      color: #111;
      cursor: pointer;
    }
    button.secondary {
      background: #2b2b2b;
      color: var(--text);
    }
    button:active {
      transform: scale(0.97);
    }
    main {
      padding: 8px;
      max-width: 1000px;
      margin: 0 auto 40px;
    }
    .card {
      background: var(--card);
      border-radius: 10px;
      padding: 10px;
      margin-bottom: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
    }
    .card h2 {
      margin: 0 0 6px;
      font-size: 15px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: var(--accent);
    }
    .card small {
      color: var(--muted);
    }
    .summary-list {
      list-style: none;
      padding-left: 0;
      margin: 6px 0 0;
      font-size: 13px;
    }
    .summary-list li {
      padding: 4px 0;
      border-bottom: 1px solid #333;
    }
    .summary-empty {
      font-size: 12px;
      color: var(--muted);
      font-style: italic;
    }
    .category {
      margin-bottom: 8px;
    }
    .category-title {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 4px;
    }
    .category-title span {
      font-size: 13px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.05em;
      color: var(--accent);
    }
    .item-row {
      display: grid;
      grid-template-columns: minmax(0, 1.7fr) 0.9fr auto auto;
      align-items: center;
      gap: 6px;
      padding: 4px 0;
      border-bottom: 1px solid #2a2a2a;
      font-size: 13px;
    }
    .item-name {
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }
    .item-row input[type="number"] {
      width: 70px;
      padding: 4px;
      border-radius: 6px;
      border: none;
      background: #f4f4f4;
      color: #000;
      text-align: center;
      font-size: 13px;
    }
    .item-row input[type="checkbox"] {
      transform: scale(1.1);
    }
    .legend {
      display: flex;
      justify-content: flex-end;
      gap: 14px;
      font-size: 10px;
      color: var(--muted);
      margin-bottom: 2px;
      flex-wrap: wrap;
    }
    .legend span {
      display: flex;
      align-items: center;
      gap: 4px;
    }
    .dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--accent);
    }
    @media (max-width: 640px) {
      .item-row {
        grid-template-columns: minmax(0, 1.8fr) 0.8fr auto auto;
        font-size: 12px;
      }
      header .title {
        font-size: 16px;
      }
    }
    @media print {
      body {
        background: #fff;
        color: #000;
      }
      header,
      .toolbar {
        display: none;
      }
      main {
        margin: 0;
        padding: 0;
      }
      .card {
        box-shadow: none;
        border: 1px solid #ccc;
      }
    }
  </style>
</head>
<body>
  <header>
    <!-- Ton logo doit s'appeler logo.png dans le repo -->
    <img src="logo.png" alt="Pause Burger Logo" />
    <div class="title-block">
      <div class="title">Inventaire</div>
      <div class="subtitle">Pause Burger · Liste de courses automatique</div>
    </div>
  </header>

  <div class="toolbar">
    <button onclick="clearAll()">Tout réinitialiser</button>
    <button class="secondary" onclick="refreshSummary()">Mettre à jour la liste</button>
    <button class="secondary" onclick="shareList()">Partager la liste</button>
    <button class="secondary" onclick="window.print()">Imprimer</button>
  </div>

  <main>
    <section class="card">
      <h2>Liste à commander</h2>
      <small>Produits cochés <b>“À commander”</b> avec une quantité &gt; 0</small>
      <ul id="summary" class="summary-list">
        <li class="summary-empty">Rien à commander pour l'instant.</li>
      </ul>
    </section>

    <section class="card">
      <div class="legend">
        <span><div class="dot"></div> Quantité à ramener</span>
        <span>☑ Inventaire fait</span>
        <span>☑ À commander</span>
      </div>
      <div id="categories"></div>
    </section>
  </main>

  <script>
    // 🧾 LISTE FIXE DES PRODUITS
    const data = {
      "Légumes": ["Salade", "Tomate", "Oignon", "Cornichon"],
      "Viandes": [
        "Steak 30g",
        "Steak 45g",
        "CB",
        "Kebab",
        "Nuggets",
        "Fricadelle",
        "Mexicains",
        "Poulet",
        "Fish",
        "Merguez",
        "Chorizo",
        "Lardons",
        "Rösti"
      ],
      "Fromages": [
        "Cheddar",
        "Raclette",
        "Chèvre",
        "Oignon frits",
        "Mozzarella",
        "Boursin",
        "Bacon",
        "Œuf",
        "Miel",
        "Sauce cheddar"
      ],
      "Sauces groupe 1": ["Mayonnaise", "Biggy", "Harissa", "Giant", "Algérienne"],
      "Sauces groupe 2": ["Samouraï", "Ketchup", "BBQ", "Andalouse", "Poivre", "Pita"],
      "Sauces groupe 3": [
        "Oignon poivron",
        "Marocaine",
        "Chili",
        "Harissa forte",
        "Tasty",
        "Smoky",
        "Curry",
        "Fish",
        "Cheezy",
        "Brazil"
      ],
      "Frites & Boîtes": [
        "Boîte frites petite",
        "Boîte frites grande",
        "Pot de sauce",
        "Boîte tenders x3",
        "Boîte tenders x6",
        "Boîte tenders x12",
        "Boîte tenders x20"
      ],
      "Spéciaux": [
        "Bouchée camembert",
        "Onion Rings",
        "Mozza Sticks",
        "Wings",
        "Wings épicé"
      ],
      "Emballages": [
        "Galette tacos grande",
        "Galette tacos petite",
        "Emballage wrap",
        "Emballage tacos",
        "Emballage grand burger",
        "Emballage petit burger"
      ],
      "Pains": [
        "Pain sésame",
        "Pain brioché",
        "Pain toast",
        "Petit pain",
        "Pain noir",
        "Pain peluche"
      ],
      "Hygiène": [
        "Essuie-tout",
        "Lave-sol",
        "Eau javel",
        "Dégraissant",
        "Serpillière",
        "Éponge inox",
        "Gants",
        "Sac poubelle",
        "Lave-mains"
      ],
      "Épicerie / Sec": [
        "Farine",
        "Épices tenders",
        "Sel",
        "Poivre",
        "Sac de congélation",
        "Papier cuisson",
        "Aluminium"
      ]
    };

    const STORAGE_KEY = "pause_burger_inventaire_v1";

    function loadState() {
      try {
        const raw = localStorage.getItem(STORAGE_KEY);
        return raw ? JSON.parse(raw) : {};
      } catch (e) {
        return {};
      }
    }

    function saveState(state) {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(state));
    }

    function clearAll() {
      if (!confirm("Tout effacer (quantités + cases cochées) ?")) return;
      localStorage.removeItem(STORAGE_KEY);
      render();
      refreshSummary();
    }

    function render() {
      const container = document.getElementById("categories");
      container.innerHTML = "";
      const state = loadState();

      Object.entries(data).forEach(([cat, items]) => {
        const catDiv = document.createElement("div");
        catDiv.className = "category";

        const catTitle = document.createElement("div");
        catTitle.className = "category-title";
        const span = document.createElement("span");
        span.textContent = cat;
        catTitle.appendChild(span);
        catDiv.appendChild(catTitle);

        items.forEach((item) => {
          const id = cat + "__" + item;
          const row = document.createElement("div");
          row.className = "item-row";

          const name = document.createElement("div");
          name.className = "item-name";
          name.textContent = item;

          const qty = document.createElement("input");
          qty.type = "number";
          qty.min = "0";
          qty.placeholder = "Qté";
          qty.value = state[id]?.qty || "";
          qty.addEventListener("input", () => {
            const s = loadState();
            if (!s[id]) s[id] = {};
            s[id].qty = qty.value;
            saveState(s);
          });

          const done = document.createElement("input");
          done.type = "checkbox";
          done.checked = !!state[id]?.done;
          done.addEventListener("change", () => {
            const s = loadState();
            if (!s[id]) s[id] = {};
            s[id].done = done.checked;
            saveState(s);
          });

          const order = document.createElement("input");
          order.type = "checkbox";
          order.checked = !!state[id]?.order;
          order.addEventListener("change", () => {
            const s = loadState();
            if (!s[id]) s[id] = {};
            s[id].order = order.checked;
            saveState(s);
            refreshSummary();
          });

          row.appendChild(name);
          row.appendChild(qty);
          row.appendChild(done);
          row.appendChild(order);
          catDiv.appendChild(row);
        });

        container.appendChild(catDiv);
      });
    }

    function buildSummary() {
      const state = loadState();
      const lines = [];
      Object.entries(data).forEach(([cat, items]) => {
        items.forEach((item) => {
          const id = cat + "__" + item;
          const s = state[id];
          if (s && s.order && s.qty && Number(s.qty) > 0) {
            const line = s.qty + " × " + item + " (" + cat + ")";
            lines.push(line);
          }
        });
      });
      return lines;
    }

    function refreshSummary() {
      const list = document.getElementById("summary");
      const lines = buildSummary();
      list.innerHTML = "";
      if (!lines.length) {
        const li = document.createElement("li");
        li.className = "summary-empty";
        li.textContent = "Rien à commander pour l'instant.";
        list.appendChild(li);
        return;
      }
      lines.forEach((text) => {
        const li = document.createElement("li");
        li.textContent = text;
        list.appendChild(li);
      });
    }

    async function shareList() {
      const lines = buildSummary();
      if (!lines.length) {
        alert("Aucun produit marqué à commander.");
        return;
      }
      const text =
        "Liste à commander - Pause Burger:\n\n" +
        lines.map((l) => "- " + l).join("\n");

      if (navigator.share) {
        try {
          await navigator.share({ text });
        } catch (e) {
          console.log("Partage annulé", e);
        }
      } else if (navigator.clipboard) {
        try {
          await navigator.clipboard.writeText(text);
          alert("Liste copiée dans le presse-papiers.");
        } catch (e) {
          alert("Impossible de partager automatiquement.\n\n" + text);
        }
      } else {
        alert(text);
      }
    }

    render();
    refreshSummary();
  </script>
</body>
</html>
