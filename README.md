# la-et-là
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercices - La vs Là</title>
    <style>
        .correct { color: green; }
        .incorrect { color: red; }
        .feedback { margin-top: 5px; }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["là", "là", "la", "là", "la", "là", "la", "la", "là", "la", "la", "là", "là", "la", "là", "la", "là", "la", "là", "la"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✅ Correct";
                    feedback.className = "correct feedback";
                    score++;
                } else {
                    feedback.innerText = `❌ Incorrect. La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "la" est un article défini féminin (ex: la maison), tandis que "là" indique un lieu (ex: pose-le là).`;
                    feedback.className = "incorrect feedback";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>
<body>
    <h2>Exercices - Complétez avec "la" ou "là"</h2>

    <p><strong>Règle :</strong> "La" est un article défini féminin qui désigne un nom (équivalent de "le" au féminin). "Là" est un adverbe de lieu qui indique un endroit précis. Exemples : "la maison" (article) et "pose-le là" (lieu).</p>

    <form>
        <ol>
            <li>Je vais ___-bas pour prendre un livre. <input type="text" id="reponse1"> <span id="feedback1"></span></li>
            <li>Pose-le juste ___, s'il te plaît. <input type="text" id="reponse2"> <span id="feedback2"></span></li>
            <li>___ voiture est rouge. <input type="text" id="reponse3"> <span id="feedback3"></span></li>
            <li>Il est parti par ___. <input type="text" id="reponse4"> <span id="feedback4"></span></li>
            <li>Je ne trouve pas ___ solution. <input type="text" id="reponse5"> <span id="feedback5"></span></li>
            <li>Elle est ___ pour te voir. <input type="text" id="reponse6"> <span id="feedback6"></span></li>
            <li>___ porte est ouverte. <input type="text" id="reponse7"> <span id="feedback7"></span></li>
            <li>Il faut nettoyer ___ cuisine. <input type="text" id="reponse8"> <span id="feedback8"></span></li>
            <li>Je l'ai vue juste ___, près de l'arbre. <input type="text" id="reponse9"> <span id="feedback9"></span></li>
            <li>___ fenêtre est cassée. <input type="text" id="reponse10"> <span id="feedback10"></span></li>
            <li>Elle aime ___ musique classique. <input type="text" id="reponse11"> <span id="feedback11"></span></li>
            <li>Regarde par ___ pour voir le jardin. <input type="text" id="reponse12"> <span id="feedback12"></span></li>
            <li>Je vais m'asseoir ___ un moment. <input type="text" id="reponse13"> <span id="feedback13"></span></li>
            <li>___ chambre est rangée. <input type="text" id="reponse14"> <span id="feedback14"></span></li>
            <li>Il est caché juste ___ ! <input type="text" id="reponse15"> <span id="feedback15"></span></li>
            <li>Elle regarde ___ télévision. <input type="text" id="reponse16"> <span id="feedback16"></span></li>
            <li>Je l'ai laissé ___ sur la table. <input type="text" id="reponse17"> <span id="feedback17"></span></li>
            <li>___ porte est lourde. <input type="text" id="reponse18"> <span id="feedback18"></span></li>
            <li>Je l'ai vu là-bas, juste ___ ! <input type="text" id="reponse19"> <span id="feedback19"></span></li>
            <li>___ lampe est très belle. <input type="text" id="reponse20"> <span id="feedback20"></span></li>
        </ol>

        <button type="button" onclick="verifier()">Vérifier</button>
    </form>

    <p id="score"></p>
</body>
</html>
