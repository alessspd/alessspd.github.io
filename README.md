<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Mi Preciosa</title>
    <style>
        body {
            background-color: #ffcccc; /* Color de fondo romántico */
            text-align: center;
            font-family: Arial, sans-serif;
            color: black;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            position: relative;
        }
        .mensaje {
            font-size: 24px;
            background: rgba(255, 255, 255, 0.7);
            padding: 20px;
            border-radius: 10px;
            display: inline-block;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }
        .botones {
            margin-top: 20px;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        button:hover {
            opacity: 0.8;
        }
        #si {
            background-color: #ff6699;
            color: white;
        }
        #no {
            background-color: #cccccc;
            position: relative;
        }
        /* Estilo para el reproductor de Spotify en la esquina inferior derecha */
        #spotifyIframe {
            position: absolute;
            bottom: 10px; /* Ajustado para que quede en la esquina inferior */
            right: 10px;  /* Ajustado para la esquina derecha */
            width: 300px;
            height: 80px;
        }
    </style>
</head>
<body>
    <div class="mensaje">
        <p>Amore, mi preciosa Lisa, eres lo mejor que me ha pasado. ¿Quieres estar conmigo por siempre?</p>
    </div>
    <div class="botones">
        <button id="si" onclick="aceptar()">Sí</button>
        <button id="no" onclick="negar()">No</button>
    </div>

    <!-- Reproductor de Spotify (Iframe) -->
    <iframe id="spotifyIframe" style="border-radius:12px" src="https://open.spotify.com/embed/track/3p4hRhMcb6ch8OLtATMaLw?utm_source=generator" width="300" height="80" frameborder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>

    <script>
        function aceptar() {
            alert("Sabia que dirias que si. Muchas gracias por darme todas las oportunidades que me das, muchas gracias por hacerme la persona mas feliz del mundo, muchas gracias por cada cosa que me demuestras, muchas gracias por ser la persona a la que mas he amado y a la que mas amare, gracias por ser la mujer de mis sueños, te adoro.");
        }

        function negar() {
            let noBtn = document.getElementById("no");

            // Hacer que el botón "No" se mueva por toda la pantalla
            let maxX = window.innerWidth - noBtn.offsetWidth; // Ancho máximo
            let maxY = window.innerHeight - noBtn.offsetHeight; // Alto máximo

            let randomX = Math.random() * maxX; // Posición aleatoria en el eje X
            let randomY = Math.random() * maxY; // Posición aleatoria en el eje Y

            // Cambiar la posición del botón "No"
            noBtn.style.position = "absolute";
            noBtn.style.left = randomX + "px";
            noBtn.style.top = randomY + "px";

            // Hacer que el tamaño del botón "No" aumente
            let size = parseInt(window.getComputedStyle(noBtn).fontSize);
            size += 10;
            noBtn.style.fontSize = size + "px";  // Aumenta el tamaño del texto
            noBtn.style.transform = "scale(1.1)";  // Aumenta el tamaño del botón

            // Si el tamaño del botón supera un valor determinado, ocultamos el botón "No"
            if (size > 100) {
                noBtn.style.display = "none";
            }
        }
    </script>
</body>
</html>
