<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Altar de Día de Muertos - Tradición y Significado</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --cempasuchil: #FF8C00;
            --morado: #4A154B;
            --morado-oscuro: #2A082C;
            --rosa-mexicano: #E91E63;
            --amarillo: #FFD700;
            --blanco: #FFF8E7;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--morado-oscuro);
            color: var(--blanco);
            line-height: 1.6;
        }

        /* Banner de Papel Picado */
        .papel-picado-banner {
            display: flex;
            justify-content: space-around;
            background-color: var(--rosa-mexicano);
            padding: 10px 0;
            overflow: hidden;
        }

        .banderines {
            width: 40px;
            height: 50px;
            background-color: var(--amarillo);
            clip-path: polygon(0 0, 100% 0, 100% 80%, 50% 100%, 0 80%);
            animation: mecer 3s infinite ease-in-out alternate;
        }

        .banderines:nth-child(even) {
            background-color: var(--cempasuchil);
            animation-delay: 0.5s;
        }

        @keyframes mecer {
            0% { transform: rotate(-5deg); }
            100% { transform: rotate(5deg); }
        }

        /* Encabezado */
        header {
            text-align: center;
            padding: 50px 20px;
            background: linear-gradient(180deg, var(--morado) 0%, var(--morado-oscuro) 100%);
        }

        header h1 {
            font-family: 'Cinzel Decorative', cursive;
            font-size: 2.5rem;
            color: var(--cempasuchil);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.1rem;
            color: var(--blanco);
        }

        /* Contenedor Principal */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Sección del Altar Interactivo */
        .seccion-altar {
            text-align: center;
            margin-bottom: 50px;
        }

        .seccion-altar h2 {
            font-family: 'Cinzel Decorative', cursive;
            color: var(--cempasuchil);
            margin-bottom: 20px;
        }

        .altar-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            margin-top: 20px;
        }

        .nivel {
            background: linear-gradient(90deg, var(--cempasuchil), var(--amarillo));
            color: #000;
            font-weight: 600;
            padding: 15px;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
        }

        .nivel:hover {
            transform: scale(1.03);
            box-shadow: 0 0 15px var(--cempasuchil);
        }

        .n1 { width: 30%; }
        .n2 { width: 40%; }
        .n3 { width: 50%; }
        .n4 { width: 60%; }
        .n5 { width: 70%; }
        .n6 { width: 80%; }
        .n7 { width: 90%; }

        /* Panel Informativo */
        #info-panel {
            margin-top: 25px;
            padding: 20px;
            background-color: var(--morado);
            border: 2px solid var(--cempasuchil);
            border-radius: 8px;
            min-height: 100px;
        }

        /* Cuadrícula de Elementos */
        .elementos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .card {
            background-color: var(--morado);
            border-radius: 8px;
            padding: 20px;
            border-left: 4px solid var(--rosa-mexicano);
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
        }

        .card h3 {
            color: var(--cempasuchil);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Pie de página */
        footer {
            text-align: center;
            padding: 20px;
            background-color: #120313;
            color: #888;
            margin-top: 50px;
        }

        /* Adaptabilidad */
        @media (max-width: 600px) {
            header h1 { font-size: 1.8rem; }
            .nivel { width: 95% !important; }
        }
    </style>
</head>
<body>

    <!-- Banner Superior Decorativo -->
    <div class="papel-picado-banner">
        <div class="banderines"></div>
        <div class="banderines"></div>
        <div class="banderines"></div>
        <div class="banderines"></div>
        <div class="banderines"></div>
        <div class="banderines"></div>
        <div class="banderines"></div>
    </div>

    <!-- Encabezado -->
    <header>
        <h1>Altar de Día de Muertos</h1>
        <p>Una tradición ancestral para honrar la memoria de nuestros seres queridos</p>
    </header>

    <div class="container">
        <!-- Sección Altar de 7 Niveles -->
        <section class="seccion-altar">
            <h2>El Altar de los 7 Niveles</h2>
            <p>Haz clic en cualquier nivel para descubrir su significado dentro de la tradición:</p>

            <div class="altar-container">
                <div class="nivel n1" onclick="mostrarInfo(1)">Nivel 1: Santo o Virgen</div>
                <div class="nivel n2" onclick="mostrarInfo(2)">Nivel 2: Ánimas del Purgatorio</div>
                <div class="nivel n3" onclick="mostrarInfo(3)">Nivel 3: La Sal (Purificación)</div>
                <div class="nivel n4" onclick="mostrarInfo(4)">Nivel 4: Pan de Muerto</div>
                <div class="nivel n5" onclick="mostrarInfo(5)">Nivel 5: Comida y Bebida Favorita</div>
                <div class="nivel n6" onclick="mostrarInfo(6)">Nivel 6: Fotografías</div>
                <div class="nivel n7" onclick="mostrarInfo(7)">Nivel 7: Cruz de Cempasúchil</div>
            </div>

            <div id="info-panel">
                <p><em>Selecciona un nivel del altar para leer más información.</em></p>
            </div>
        </section>

        <!-- Sección Elementos Principales -->
        <section>
            <h2 style="text-align: center; color: var(--cempasuchil); font-family: 'Cinzel Decorative', cursive; margin-bottom: 20px;">
                Elementos Imprescindibles
            </h2>
            <div class="elementos-grid">
                <div class="card">
                    <h3>🕯️ Velas y Veladoras</h3>
                    <p>Representan la luz, la fe y la esperanza. Guían a las almas para que puedan llegar a sus antiguos hogares y regresar a su camino.</p>
                </div>
                <div class="card">
                    <h3>🌼 Flor de Cempasúchil</h3>
                    <p>Su color brillante y aroma característico trazan el camino que las almas deben seguir para no perderse durante su visita.</p>
                </div>
                <div class="card">
                    <h3>💀 Calaveritas de Azúcar</h3>
                    <p>Aluden a la muerte siempre presente. Llevan inscritos en la frente los nombres de las personas recordadas o de los vivos como juego festivo.</p>
                </div>
                <div class="card">
                    <h3>🍞 Pan de Muerto</h3>
                    <p>Representa la fraternidad y el cuerpo del difunto. Su forma circular simboliza el ciclo de la vida y la muerte.</p>
                </div>
                <div class="card">
                    <h3>🧪 Agua y Sal</h3>
                    <p>El agua calma la sed del espíritu tras su largo viaje. La sal es un elemento de purificación que evita que el alma se corrompa.</p>
                </div>
                <div class="card">
                    <h3>✂️ Papel Picado</h3>
                    <p>Representa el aire, uno de los cuatro elementos naturales presentes en la ofrenda. Además, añade alegría y color festivo.</p>
                </div>
            </div>
        </section>
    </div>

    <!-- Pie de Página -->
    <footer>
        <p>© 2026 Proyecto Educativo - Tradiciones de México: Día de Muertos</p>
    </footer>

    <!-- Lógica de Interacción -->
    <script>
        const datosNiveles = {
            1: "<strong>Primer Nivel:</strong> Se coloca la imagen del santo o virgen del cual se sea devoto para protección de la ofrenda.",
            2: "<strong>Segundo Nivel:</strong> Destinado a las ánimas del purgatorio. Permite que el alma del difunto obtenga permiso para salir de ese lugar.",
            3: "<strong>Tercer Nivel:</strong> Se coloca la sal para purificar el espíritu de los niños o adultos y para que el cuerpo no se corrompa en el viaje.",
            4: "<strong>Cuarto Nivel:</strong> El elemento principal es el Pan de Muerto, que simboliza la consagración y el alimento espiritual.",
            5: "<strong>Quinto Nivel:</strong> Se colocan los alimentos, frutas y platillos favoritos que le gustaban al difunto en vida.",
            6: "<strong>Sexto Nivel:</strong> Reservado para las fotografías de las personas fallecidas a quienes se les dedica la ofrenda.",
            7: "<strong>Séptimo Nivel:</strong> Se coloca una cruz formada por flores de cempasúchil, ceniza o cal, para expiar sus culpas pendientes."
        };

        function mostrarInfo(nivel) {
            const panel = document.getElementById('info-panel');
            panel.innerHTML = `<p>${datosNiveles[nivel]}</p>`;
        }
    </script>
</body>
</html>