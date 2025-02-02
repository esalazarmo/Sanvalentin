<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        .botones {
            margin-top: 30px;
        }
        #no {
            position: relative;
            display: inline-block;
            cursor: pointer;
            transition: 0.2s;
        }
        #no:hover {
            position: absolute;
            left: 50px;
            top: -30px;
        }
        #si {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        #no:active {
            cursor: not-allowed;
        }
    </style>
</head>
<body>

    <h1>¿Quieres ser mi San Valentín, Millen?</h1>

    <div class="botones">
        <button id="si">Sí</button>
        <button id="no" onmousedown="moverNo()">No</button>
    </div>

    <script>
        function moverNo() {
            // El botón "No" se mueve ligeramente al ser presionado
            let noButton = document.getElementById('no');
            let currentLeft = parseInt(window.getComputedStyle(noButton).left, 10) || 0;
            noButton.style.left = (currentLeft + 50) + 'px';
            noButton.style.top = '-30px';
        }
    </script>

</body>
</html>
