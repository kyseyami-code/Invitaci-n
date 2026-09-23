# Invitaci-n
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kenia's Party</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #050505;
            color: #ffffff;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Capa de inicio para asegurar la reproducción de música */
        #welcome-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #000;
            z-index: 9999;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            cursor: pointer;
        }

        #welcome-overlay h2 {
            color: #ffd700;
            font-size: 2rem;
            margin-bottom: 10px;
            font-family: 'Georgia', serif;
        }

        #welcome-overlay p {
            color: #aaa;
            font-size: 1rem;
        }

        /* Contenedor con efecto de destellos radiantes */
        .invitation-card {
            width: 100%;
            max-width: 420px;
            background: radial-gradient(circle at center, #1f1a0e 0%, #080808 80%);
            border: 2px solid #f1c40f;
            border-radius: 20px;
            padding: 35px 25px;
            text-align: center;
            box-shadow: 0px 0px 35px rgba(241, 196, 15, 0.4);
            position: relative;
            box-sizing: border-box;
            margin: 20px;
        }

        /* Título con resplandor */
        h1 {
            font-family: 'Georgia', serif;
            color: #ffd700;
            font-size: 2.6rem;
            margin: 0 0 10px 0;
            text-shadow: 0 0 12px rgba(255, 215, 0, 0.7);
        }

        .subtitle {
            font-size: 1.15rem;
            color: #f0e6d2;
            margin-top: 15px;
            margin-bottom: 25px;
            line-height: 1.5;
        }

        .date-time {
            background: linear-gradient(135deg, rgba(241, 196, 15, 0.2), rgba(0, 0, 0, 0.6));
            border: 1px solid #ffd700;
            border-radius: 12px;
            padding: 14px;
            font-size: 1.25rem;
            font-weight: bold;
            color: #ffd700;
            margin-bottom: 20px;
            text-shadow: 0 0 5px rgba(0,0,0,0.8);
        }

        .details {
            font-size: 1.05rem;
            color: #dddddd;
            margin-bottom: 20px;
            line-height: 1.4;
        }

        .important-note {
            font-size: 0.95rem;
            color: #ffd700;
            background: rgba(255, 215, 0, 0.08);
            border-left: 3px solid #ffd700;
            padding: 10px 15px;
            border-radius: 6px;
            margin-bottom: 25px;
            text-align: left;
        }

        .btn {
            display: block;
            width: 100%;
            padding: 14px 0;
            margin: 12px 0;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1rem;
            transition: transform 0.2s, box-shadow 0.3s;
            box-sizing: border-box;
        }

        .btn-whatsapp {
            background: linear-gradient(45deg, #25d366, #128c7e);
            color: white;
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.3);
        }

        .btn-map {
            background: linear-gradient(45deg, #ffd700, #d4af37);
            color: #000;
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }

        .btn:hover {
            transform: translateY(-2px);
        }
    </style>
</head>
<body>

    <!-- Capa que activa el audio automáticamente al hacer clic -->
    <div id="welcome-overlay" onclick="startInvitation()">
        <h2>✨ Kenia's Party ✨</h2>
        <p>Toca la pantalla para abrir la invitación ✉️</p>
    </div>

    <!-- Elemento de audio automático oculto -->
    <audio id="bg-music" loop preload="auto">
        <!-- Reemplaza el enlace con el archivo MP3 directo de tu canción favorita (ej. Memories) -->
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>

    <div class="invitation-card">
        <h1>✨ Kenia's Party ✨</h1>
        
        <p class="subtitle">
            ¡Vamos a festejar que ya soy <strong>Maestra</strong> y de paso <strong>Mi Cumple</strong>! 🎉🎓
        </p>

        <div class="date-time">
            📅 3 de octubre 2026<br>
            ⏰ 4:00 p.m.
        </div>

        <div class="details">
            📍 <strong>Ubicación:</strong><br>
            Chapultepec s/n, San Fco. Tlalcilalcalpan
        </div>

        <div class="important-note">
            ⏳ <em>Llega con tiempo, la comida se servirá de 5:00 a 7:00 p.m.</em>
        </div>

        <!-- Confirmación por WhatsApp -->
        <a href="https://wa.me/?text=¡Hola%20Kenia!%20Confirmo%20mi%20asistencia%20para%20tu%20fiesta." 
           class="btn btn-whatsapp" target="_blank">
            💬 Confirmar por WhatsApp
        </a>

        <!-- Ubicación en Google Maps -->
        <a href="https://www.google.com/maps/search/?api=1&query=Chapultepec+San+Francisco+Tlalcilalcalpan" 
           class="btn btn-map" target="_blank">
            🗺️ Ver en Google Maps
        </a>
    </div>

    <script>
        function startInvitation() {
            var audio = document.getElementById("bg-music");
            audio.play();
            document.getElementById("welcome-overlay").style.display = "none";
        }
    </script>

</body>
</html>
