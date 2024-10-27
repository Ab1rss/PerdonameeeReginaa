# PerdonameeeReginaa
Peroname mi niña 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Me perdonas?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
            text-align: center;
        }

        h1 {
            font-size: 24px;
            margin-bottom: 20px;
        }

        .buttons {
            display: flex;
            gap: 20px;
            align-items: center;
        }

        .button {
            padding: 15px 25px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        #yesButton {
            background-color: #4CAF50;
            color: white;
        }

        #noButton {
            background-color: #f44336;
            color: white;
        }

        .cat-image {
            width: 150px;
            height: auto;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <!-- Imagen del gatito suplicante -->
    <img src="https://media.giphy.com/media/VbnUQpnihPSIgIXuZv/giphy.gif" alt="Gatito Suplicando" class="cat-image">

    <h1>¿Me perdonas?</h1>
    <div class="buttons">
        <button id="yesButton" class="button" onclick="showLoveMessage()">SÍ!!!</button>
        <button id="noButton" class="button" onclick="handleNoClick()">¿Pero segura, segura?</button>
    </div>
    <p id="message" style="margin-top: 20px;"></p>

    <script>
        let noMessages = [
            "¿Estás segura?",
            "Muy, muy segura?",
            "Por favor, perdóname",
            "No seas tan dura conmigo",
            "Sabes que te adoro, ¿verdad?",
            "Ándale, enana, perdóname",
            "Solo quiero verte sonreír",
            "Vamos, dame una oportunidad",
            "Por favor, ¿sí?"
        ];

        let noClickCount = 0;
        let yesButton = document.getElementById("yesButton");
        let message = document.getElementById("message");

        function handleNoClick() {
            // Cambiar el mensaje en el botón "No"
            document.getElementById("noButton").textContent = noMessages[noClickCount] || "Por favor, perdóname";

            // Incrementar el tamaño del botón "Sí"
            yesButton.style.transform = `scale(${1 + noClickCount * 0.1})`;

            // Incrementar el contador
            noClickCount++;
        }

        function showLoveMessage() {
            // Mostrar el mensaje final
            message.textContent = "Yo sabía que ibas a perdonarme tan fácilmente, te amo, princesita linda.";
            // Ocultar los botones
            document.querySelector('.buttons').style.display = 'none';
        }
    </script>
</body>
</html>