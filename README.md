<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Flores para Sher</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
        background: #fff0f5;
        margin: 0;
        padding: 50px;
        overflow-x: hidden;
    }

    a {
        display: inline-block;
        padding: 10px 20px;
        background: #ff69b4;
        color: white;
        text-decoration: none;
        border-radius: 20px;
        font-size: 18px;
        transition: 0.3s;
    }
    a:hover {
        background: #ff1493;
    }

    #mensaje {
        display: none;
        font-size: 28px;
        color: #d63384;
        margin-top: 30px;
        animation: aparecer 1s ease-in-out;
    }

    /* Animación de caída */
    @keyframes caer {
        0% { transform: translateY(-100px) rotate(0deg); opacity: 1; }
        100% { transform: translateY(110vh) rotate(360deg); opacity: 0; }
    }

    @keyframes aparecer {
        from { opacity: 0; }
        to { opacity: 1; }
    }

    .flor {
        position: absolute;
        font-size: 30px;
        animation: caer linear;
    }
</style>
</head>
<body>

<h1>🌷 Flores para ti 🌹</h1>
<a href="#" onclick="mostrarFlores()">Haz clic aquí</a>

<div id="mensaje">💖 Ten por bonita Sher 💖</div>

<script>
function mostrarFlores() {
    // Mostrar el mensaje
    document.getElementById("mensaje").style.display = "block";

    // Crear flores animadas
    const flores = ["🌹", "🌷"];
    for (let i = 0; i < 20; i++) {
        let flor = document.createElement("div");
        flor.classList.add("flor");
        flor.textContent = flores[Math.floor(Math.random() * flores.length)];
        flor.style.left = Math.random() * window.innerWidth + "px";
        flor.style.animationDuration = (Math.random() * 3 + 2) + "s";
        document.body.appendChild(flor);

        // Eliminar después de la animación
        setTimeout(() => {
            flor.remove();
        }, 5000);
    }
}
</script>

</body>
</html>
