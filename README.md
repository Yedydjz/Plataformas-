<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Slot Machine</title>
    <style>
        /* Adicione estilos CSS aqui */
        /* Você pode personalizar o layout e o design de acordo com suas preferências */
    </style>
</head>
<body>
    <h1>Slot Machine</h1>
    <div id="slotMachine">
        <div class="slot" id="slot1"></div>
        <div class="slot" id="slot2"></div>
        <div class="slot" id="slot3"></div>
    </div>
    <button onclick="spin()">Spin</button>

    <script>
        // Adicione scripts JavaScript aqui
        // Você pode implementar a lógica de funcionamento da máquina de slots aqui

        // Array com os ícones dos slots
        const symbols = ['cherry', 'banana', 'apple', 'orange', 'lemon'];

        function spin() {
            // Gera aleatoriamente um ícone para cada slot
            const result1 = Math.floor(Math.random() * symbols.length);
            const result2 = Math.floor(Math.random() * symbols.length);
            const result3 = Math.floor(Math.random() * symbols.length);

            // Atualiza visualmente os ícones dos slots
            document.getElementById('slot1').style.backgroundImage = `url('${symbols[result1]}.png')`;
            document.getElementById('slot2').style.backgroundImage = `url('${symbols[result2]}.png')`;
            document.getElementById('slot3').style.backgroundImage = `url('${symbols[result3]}.png')`;

            // Verifica se houve uma combinação vencedora
            if (result1 === result2 && result2 === result3) {
                alert('Congratulations! You win!');
            } else {
                alert('Try again!');
            }
        }
    </script>
</body>
</html>
