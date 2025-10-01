# CITATION---APP-
Citation app<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Citations Aléatoires</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f3f3f3;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .container {
      background: white;
      padding: 30px;
      border-radius: 12px;
      text-align: center;
      box-shadow: 0px 4px 10px rgba(0,0,0,0.1);
      width: 400px;
    }
    h1 {
      font-size: 22px;
      margin-bottom: 20px;
      color: #444;
    }
    .quote {
      font-style: italic;
      font-size: 18px;
      margin-bottom: 15px;
      color: #333;
    }
    .author {
      font-weight: bold;
      color: #666;
      margin-bottom: 20px;
    }
    button {
      padding: 10px 20px;
      border: none;
      background: #007BFF;
      color: white;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
    }
    button:hover {
      background: #0056b3;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>💡 Citation du jour</h1>
    <p class="quote">Clique sur le bouton pour voir une citation</p>
    <p class="author"></p>
    <button onclick="nouvelleCitation()">Nouvelle citation</button>
  </div>

  <script>
    const citations = [
      { texte: "Le succès est la somme de petits efforts répétés jour après jour.", auteur: "Robert Collier" },
      { texte: "La meilleure façon de prédire l’avenir est de le créer.", auteur: "Peter Drucker" },
      { texte: "Ils ne savaient pas que c’était impossible, alors ils l’ont fait.", auteur: "Mark Twain" },
      { texte: "Le bonheur n’est pas quelque chose de prêt à l’emploi. Il vient de vos propres actions.", auteur: "Dalaï Lama" },
      { texte: "Croyez en vos rêves et ils se réaliseront peut-être. Croyez en vous et ils se réaliseront sûrement.", auteur: "Martin Luther King" }
    ];

    function nouvelleCitation() {
      const index = Math.floor(Math.random() * citations.length);
      const citation = citations[index];
      document.querySelector(".quote").textContent = "“" + citation.texte + "”";
      document.querySelector(".author").textContent = "- " + citation.auteur;
    }
  </script>
</body>
</html>
