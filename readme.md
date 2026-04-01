<!DOCTYPE html>
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <title>The Goblin Game</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #081c15, #1b4332, #2d6a4f);
            color: white;
            text-align: center;
            min-height: 100vh;
        }

        /* ---- PAGES ---- */
        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        /* ---- HEADER ---- */
        header {
            padding: 25px 40px;
            background: rgba(0, 0, 0, 0.3);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        header h1 {
            font-size: 32px;
            color: #95ff9b;
        }

        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: white;
            font-size: 17px;
            cursor: pointer;
        }

        nav a:hover {
            color: #95ff9b;
        }

        /* ---- HERO ---- */
        .hero {
            padding: 90px 20px 70px;
        }

        .hero h2 {
            font-size: 52px;
            color: #caffbf;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 18px;
            max-width: 580px;
            margin: 0 auto 40px;
            line-height: 1.7;
            color: rgba(255, 255, 255, 0.8);
        }

        button {
            padding: 14px 36px;
            font-size: 17px;
            border: none;
            border-radius: 30px;
            background: linear-gradient(90deg, #52b788, #95ff9b);
            color: #081c15;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            transform: scale(1.05);
        }

        /* ---- FOOTER ---- */
        footer {
            margin-top: 60px;
            padding: 20px;
            opacity: 0.6;
            font-size: 14px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* ========================
           PAGE HISTOIRE
        ======================== */

        .histoire-hero {
            padding: 60px 20px 30px;
        }

        .histoire-hero h2 {
            font-size: 42px;
            color: #caffbf;
            margin-bottom: 10px;
        }

        .histoire-hero p {
            font-size: 16px;
            color: rgba(255, 255, 255, 0.6);
        }

        /* Blocs de chapitres */
        .chapitres {
            max-width: 900px;
            margin: 40px auto;
            padding: 0 30px;
            text-align: left;
        }

        .chapitre {
            background: rgba(255, 255, 255, 0.05);
            border-left: 4px solid #52b788;
            border-radius: 10px;
            padding: 28px 30px;
            margin-bottom: 28px;
        }

        .chapitre h3 {
            color: #95ff9b;
            font-size: 20px;
            margin-bottom: 14px;
        }

        .chapitre p {
            color: rgba(255, 255, 255, 0.8);
            font-size: 16px;
            line-height: 1.8;
        }

        /* Mondes */
        .mondes {
            max-width: 900px;
            margin: 0 auto 40px;
            padding: 0 30px;
        }

        .mondes h3 {
            color: #caffbf;
            font-size: 22px;
            margin-bottom: 20px;
            text-align: center;
        }

        .monde-liste {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
        }

        .monde-item {
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(149, 255, 155, 0.2);
            border-radius: 10px;
            padding: 16px 22px;
            width: 155px;
            text-align: center;
        }

        .monde-item .icone {
            font-size: 32px;
            margin-bottom: 8px;
        }

        .monde-item p {
            font-size: 13px;
            color: rgba(255, 255, 255, 0.7);
        }

        .monde-item strong {
            color: #95ff9b;
            font-size: 14px;
        }

        /* Citation finale */
        .citation {
            max-width: 700px;
            margin: 10px auto 20px;
            padding: 24px 30px;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 12px;
            font-style: italic;
            color: rgba(255, 255, 255, 0.7);
            font-size: 16px;
            line-height: 1.7;
        }
    </style>
</head>

<body>

    <!-- ========================
         PAGE ACCUEIL
    ======================== -->
    <div id="page-accueil" class="page active">

        <header>
            <h1>🌿 The Goblin Game</h1>
            <nav>
                <a onclick="allerA('accueil')">Accueil</a>
                <a onclick="allerA('histoire')">Histoire</a>
            </nav>
        </header>

        <section class="hero">
            <h2>Défends la Terre</h2>
            <p>
                Une menace venue de l'espace menace de détruire la vie sur Terre.
                Tu es le dernier rempart. Traverse 5 mondes et protège l'énergie vitale
                de notre planète.
            </p>
            <button onclick="allerA('histoire')">Découvrir l'histoire</button>
        </section>

        <footer>
            <p>The Goblin Game © 2026 — Dan &amp; Louis</p>
        </footer>

    </div>

    <!-- ========================
         PAGE HISTOIRE
    ======================== -->
    <div id="page-histoire" class="page">

        <header>
            <h1>🌿 The Goblin Game</h1>
            <nav>
                <a onclick="allerA('accueil')">Accueil</a>
                <a onclick="allerA('histoire')">Histoire</a>
            </nav>
        </header>

        <section class="histoire-hero">
            <h2>📖 L'Histoire</h2>
            <p>Comment tout a commencé...</p>
        </section>

        <div class="chapitres">

            <div class="chapitre">
                <h3>🌌 La menace venue des étoiles</h3>
                <p>
                    Depuis des millénaires, une entité extraterrestre erre dans l'univers
                    à la recherche d'une chose : l'énergie vitale. Cette énergie, présente
                    dans chaque être vivant, chaque arbre, chaque goutte d'eau, est la
                    ressource la plus précieuse du cosmos. Et la Terre en regorge.
                </p>
            </div>

            <div class="chapitre">
                <h3>👾 La possession</h3>
                <p>
                    Pour ne pas se montrer directement, les extraterrestres ont trouvé
                    une méthode redoutable : ils prennent possession des êtres vivants
                    et des éléments naturels de la planète. Arbres, animaux, pierres...
                    tout peut devenir leur marionnette. C'est ainsi que sont nés les goblins :
                    des créatures ordinaires transformées en soldats au service d'une volonté
                    étrangère, chargés de drainer l'énergie vitale de la Terre.
                </p>
            </div>

            <div class="chapitre">
                <h3>⚔️ Ton rôle</h3>
                <p>
                    Tu es l'un des rares humains à avoir compris ce qui se passe vraiment.
                    Ta mission : traverser les 5 grands environnements de la planète,
                    éliminer les créatures possédées vague après vague, et empêcher
                    les extraterrestres de vider la Terre de son énergie.
                    Au fil des niveaux, tu découvriras la vérité sur leur origine...
                    et peut-être une façon de les arrêter définitivement.
                </p>
            </div>

        </div>

        <div class="mondes">
            <h3>🗺️ Les 5 mondes</h3>
            <div class="monde-liste">
                <div class="monde-item">
                    <div class="icone">🌲</div>
                    <strong>La Forêt</strong>
                    <p>Niveaux 1 à 10</p>
                </div>
                <div class="monde-item">
                    <div class="icone">🏜️</div>
                    <strong>Le Désert</strong>
                    <p>Niveaux 11 à 20</p>
                </div>
                <div class="monde-item">
                    <div class="icone">🏝️</div>
                    <strong>L'Île</strong>
                    <p>Niveaux 21 à 30</p>
                </div>
                <div class="monde-item">
                    <div class="icone">⛰️</div>
                    <strong>La Montagne</strong>
                    <p>Niveaux 31 à 40</p>
                </div>
                <div class="monde-item">
                    <div class="icone">🚀</div>
                    <strong>L'Espace</strong>
                    <p>Niveaux 41 à 50</p>
                </div>
            </div>
        </div>

        <div class="citation">
            "Ils ne détruisent pas. Ils volent. Et ce qu'ils volent, c'est la vie elle-même.
            Chaque vague d'ennemis, chaque créature possédée, rapproche la Terre de son
            dernier souffle. Tu es notre seul espoir."
        </div>

        <footer>
            <p>The Goblin Game © 2026 — Dan &amp; Louis</p>
        </footer>

    </div>

    <script>
        function allerA(page) {
            document.querySelectorAll('.page').forEach(function(p) {
                p.classList.remove('active');
            });
            document.getElementById('page-' + page).classList.add('active');
            window.scrollTo(0, 0);
        }
    </script>

</body>

</html>
