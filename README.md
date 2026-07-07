
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>✨ Feliz Cumpleaños, Mi Amor ✨</title>
    <!-- Cargamos tipografías románticas y modernas de Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@700&family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        /* --- ESTILOS GENERALES Y CONFIGURACIÓN --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Quicksand', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #ffeef4, #ffd3e2, #ffb3d1);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* --- CONTENEDOR PRINCIPAL DE LAS PÁGINAS --- */
        .tarjeta-container {
            width: 90%;
            max-width: 550px;
            height: 600px;
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(8px);
            border-radius: 30px;
            box-shadow: 0 15px 45px rgba(255, 105, 180, 0.25);
            border: 3px solid #ffccd5;
            padding: 30px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            position: relative;
            z-index: 10;
            overflow: hidden;
        }

        /* --- SISTEMA DE PÁGINAS --- */
        .pagina {
            display: none; /* Ocultas por defecto */
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            width: 100%;
            height: 100%;
            animation: fadeIn 0.8s ease-in-out forwards;
        }

        .pagina.activa {
            display: flex; /* Solo se muestra la página activa */
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* --- ANIMACIONES DE DIBUJITOS --- */
        .dibujo-animado {
            font-size: 5.5rem;
            margin: 15px 0;
            display: inline-block;
            animation: flotarYRebotar 4s ease-in-out infinite;
        }

        .latido {
            display: inline-block;
            animation: latirCorazon 1.5s infinite alternate;
        }

        @keyframes flotarYRebotar {
            0%, 100% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-15px) rotate(5deg);
            }
        }

        @keyframes latirCorazon {
            0% { transform: scale(1); }
            100% { transform: scale(1.15); }
        }

        /* --- TEXTOS --- */
        .titulo-carta {
            font-family: 'Caveat', cursive;
            font-size: 2.8rem;
            color: #ff3385;
            margin-bottom: 15px;
            line-height: 1.1;
        }

        .texto-carta {
            font-size: 1.1rem;
            color: #5d4f55;
            line-height: 1.6;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .amor-resaltado {
            color: #ff0066;
            font-size: 1.3rem;
            font-weight: 700;
            display: block;
            margin-top: 10px;
        }

        /* --- BOTONES --- */
        .botones-nav {
            display: flex;
            gap: 15px;
            width: 100%;
            justify-content: center;
            margin-top: 15px;
        }

        .btn {
            background: linear-gradient(135deg, #ff66a3, #ff3385);
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 1rem;
            font-weight: 700;
            border-radius: 25px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(255, 51, 133, 0.4);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(255, 51, 133, 0.6);
            background: linear-gradient(135deg, #ff3385, #e6005c);
        }

        .btn-secundario {
            background: #ffe6f0;
            color: #ff3385;
            border: 2px solid #ffb3d1;
        }

        .btn-secundario:hover {
            background: #ffd3e2;
            color: #e6005c;
        }

        /* Botón interactivo final */
        .btn-magico {
            background: linear-gradient(135deg, #ff33cc, #9933ff);
            box-shadow: 0 5px 15px rgba(153, 51, 255, 0.4);
        }
        .btn-magico:hover {
            background: linear-gradient(135deg, #9933ff, #ff33cc);
            box-shadow: 0 8px 20px rgba(153, 51, 255, 0.6);
        }

        /* --- CORAZONES FLOTANTES DE FONDO --- */
        .corazon-flotante {
            position: absolute;
            bottom: -50px;
            color: rgba(255, 51, 133, 0.6);
            font-size: 24px;
            pointer-events: none;
            z-index: 1;
            animation: subirCorazon linear infinite;
        }

        @keyframes subirCorazon {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.8;
            }
            90% {
                opacity: 0.8;
            }
            100% {
                transform: translateY(-110vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* --- ESTRELLAS PARPADEANTES --- */
        .estrella {
            position: absolute;
            color: #fffbcf;
            font-size: 20px;
            pointer-events: none;
            z-index: 1;
            animation: parpadear 2.5s infinite ease-in-out;
        }

        @keyframes parpadear {
            0%, 100% { opacity: 0.2; transform: scale(0.8); }
            50% { opacity: 1; transform: scale(1.2); }
        }
    </style>
</head>
<body>

    <!-- Contenedor de la Tarjeta Interactiva -->
    <div class="tarjeta-container">

        <!-- ================= PÁGINA 1 ================= -->
        <div class="pagina activa" id="pag1">
            <h1 class="titulo-carta">🎉 ¡Feliz Cumpleaños, Mi Amor! 🎉</h1>
            
            <!-- Dibujo con movimiento -->
            <div class="dibujo-animado">🎂🎈🎁</div>
            
            <p class="texto-carta">
                Hoy celebramos el día en que nació la niña más maravillosa, la que llena todos mis días de felicidad, locura y un amor infinito.
            </p>
            <p class="texto-carta">
                Quiero que hoy sonrías muchísimo porque este día está hecho para consentirte y recordarte lo especial que eres.
            </p>
            <span class="amor-resaltado latido">¡Te amo con todo mi corazón! ❤️</span>

            <div class="botones-nav">
                <button class="btn" onclick="cambiarPagina(2)">Abrir Carta 💌</button>
            </div>
        </div>

        <!-- ================= PÁGINA 2 ================= -->
        <div class="pagina" id="pag2">
            <h1 class="titulo-carta">💌 Eres mi Persona Favorita 💌</h1>
            
            <div class="dibujo-animado">💑✨💖</div>
            
            <p class="texto-carta">
                Le doy gracias a la vida por haberte puesto en mi camino. Admiro tu fuerza, tu carisma, la ternura de tus abrazos y esa forma única que tienes de hacerme sonreír.
            </p>
            <p class="texto-carta">
                Deseo que este año nuevo de vida venga cargado de sueños cumplidos, metas alcanzadas y risas inolvidables. ¡Yo estaré ahí para apoyarte en cada paso!
            </p>
            <span class="amor-resaltado">¡Eres mi reina hermosa! 👑</span>

            <div class="botones-nav">
                <button class="btn btn-secundario" onclick="cambiarPagina(1)">Atrás</button>
                <button class="btn" onclick="cambiarPagina(3)">Siguiente Sorpresa 🎁</button>
            </div>
        </div>

        <!-- ================= PÁGINA 3 ================= -->
        <div class="pagina" id="pag3">
            <h1 class="titulo-carta">💍 Hoy, Mañana y Siempre 💍</h1>
            
            <div class="dibujo-animado">🧸💐💓</div>
            
            <p class="texto-carta">
                Este es solo el comienzo de muchísimos cumpleaños más que quiero celebrar de tu mano. No olvides nunca lo valiosa que eres y lo mucho que me importas.
            </p>
            <p class="texto-carta">
                Espero que te haya gustado este pequeño detalle que hice pensando en ti con todo mi amor. 
            </p>
            
            <!-- Botón interactivo que lanza explosión de corazones -->
            <button class="btn btn-magico latido" onclick="explosionDeCorazones()">¡Presiona para más Amor! 💖</button>

            <div class="botones-nav">
                <button class="btn btn-secundario" onclick="cambiarPagina(2)">Atrás</button>
                <button class="btn" onclick="reiniciarCarta()">Volver al Inicio 🔄</button>
            </div>
        </div>

    </div>

    <!-- --- CÓDIGO JAVASCRIPT --- -->
    <script>
        // Cambiar entre páginas con botones
        function cambiarPagina(numeroPagina) {
            // Ocultamos todas las páginas
            const paginas = document.querySelectorAll('.pagina');
            paginas.forEach(pag => pag.classList.remove('activa'));

            // Mostramos la página seleccionada
            const paginaDestino = document.getElementById('pag' + numeroPagina);
            if (paginaDestino) {
                paginaDestino.classList.add('activa');
            }
        }

        // Reiniciar la experiencia
        function reiniciarCarta() {
            cambiarPagina(1);
            // Lanzar una pequeña explosión de alegría al volver
            explosionDeCorazones();
        }

        // Generador de corazones flotantes continuos en el fondo
        function crearCorazon() {
            const corazon = document.createElement('div');
            corazon.classList.add('corazon-flotante');
            
            // Variedad de emojis de amor
            const tiposDeCorazon = ['❤️', '💖', '💕', '💗', '💘', '🌸', '✨'];
            corazon.innerText = tiposDeCorazon[Math.floor(Math.random() * tiposDeCorazon.length)];
            
            // Posiciones y tamaños aleatorios
            corazon.style.left = Math.random() * 100 + "vw";
            corazon.style.fontSize = Math.random() * 20 + 15 + "px";
            
            // Duración aleatoria de la animación de subida (entre 5 y 10 segundos)
            const duracion = Math.random() * 5 + 5;
            corazon.style.animationDuration = duracion + "s";
            
            document.body.appendChild(corazon);
            
            // Se elimina el elemento cuando termina la animación para no saturar
            setTimeout(() => {
                corazon.remove();
            }, duracion * 1000);
        }

        // Crear corazones flotantes de fondo automáticamente de forma continua
        setInterval(crearCorazon, 400);

        // Crear estrellas decorativas estáticas que parpadean
        function crearEstrellas() {
            for(let i = 0; i < 20; i++) {
                const estrella = document.createElement('div');
                estrella.classList.add('estrella');
                estrella.innerText = '✨';
                estrella.style.left = Math.random() * 100 + "vw";
                estrella.style.top = Math.random() * 100 + "vh";
                estrella.style.animationDelay = Math.random() * 2 + "s";
                document.body.appendChild(estrella);
            }
        }
        crearEstrellas();

        // Función interactiva de la página 3 (Explosión de corazones al pulsar botón)
        function explosionDeCorazones() {
            for (let i = 0; i < 35; i++) {
                setTimeout(() => {
                    const corazon = document.createElement('div');
                    corazon.classList.add('corazon-flotante');
                    
                    const tiposDeCorazon = ['❤️', '💖', '💕', '💗', '💘', '💝', '✨', '🌹'];
                    corazon.innerText = tiposDeCorazon[Math.floor(Math.random() * tiposDeCorazon.length)];
                    
                    // Concentrar la salida de corazones en la zona del botón
                    corazon.style.left = (Math.random() * 60 + 20) + "vw";
                    corazon.style.fontSize = Math.random() * 25 + 20 + "px";
                    
                    // Velocidad de subida rápida para simular explosión
                    const duracion = Math.random() * 3 + 2;
                    corazon.style.animationDuration = duracion + "s";
                    
                    document.body.appendChild(corazon);
                    
                    setTimeout(() => {
                        corazon.remove();
                    }, duracion * 1000);
                }, i * 50); // Pequeño desfase para que salgan en ráfaga
            }
        }
    </script>
</body>
</html>

```
