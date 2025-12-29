<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Bruliss</title>

<style>
    body {
        margin: 0;
        background-color: #ffd6e7; /* Rosado pastel */
        font-family: "Arial Rounded MT", Arial, sans-serif;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        overflow: hidden;
    }

    /* Texto superior */
    h1 {
        color: #b30059;
        font-size: 55px;
        margin-top: 25px;
        font-weight: bold;
        text-shadow: 0px 0px 6px #ffffff;
    }

    /* Texto inferior */
    h2 {
        color: #b30059;
        font-size: 38px;
        margin-bottom: 30px;
        text-shadow: 0px 0px 6px #ffffff;
    }

    /* Corazones */
    .corazon {
        position: absolute;
        color: #ff5c99;
        font-size: 20px;
        opacity: 0.9;
        animation: flotar 6s infinite ease-in-out;
    }

    @keyframes flotar {
        0% { transform: translateY(100vh) rotate(0deg); }
        100% { transform: translateY(-120vh) rotate(360deg); }
    }
</style>

</head>
<body>

    <!-- Mensaje superior -->
    <h1>Bruliss 💖</h1>

    <!-- Mensaje inferior -->
    <h2>Con cariño 💗</h2>

<script>
    /* Generador de corazones flotantes */
    function crearCorazon() {
        const corazon = document.createElement("div");
        corazon.classList.add("corazon");
        corazon.innerHTML = "❤️";
        corazon.style.left = Math.random() * 100 + "vw";
        corazon.style.fontSize = (Math.random() * 60 + 20) + "px";
        corazon.style.animationDuration = (Math.random() * 4 + 4) + "s";

        document.body.appendChild(corazon);

        setTimeout(() => {
            corazon.remove();
        }, 9000);
    }

    setInterval(crearCorazon, 250);
</script>

</body>
</html>
