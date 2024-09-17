<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LIFO y FIFO</title>
</head>
<body>
    <h1>Pilas y Colas: LIFO y FIFO</h1>

    <!-- Sección LIFO (Pila) -->
    <h2>Pila LIFO (Last In, First Out)</h2>
    <button onclick="pushToStack()">Agregar a la Pila</button>
    <button onclick="popFromStack()">Quitar de la Pila</button>
    <p id="stackDisplay">Pila: []</p>

    <!-- Sección FIFO (Cola) -->
    <h2>Cola FIFO (First In, First Out)</h2>
    <button onclick="enqueueToQueue()">Agregar a la Cola</button>
    <button onclick="dequeueFromQueue()">Quitar de la Cola</button>
    <p id="queueDisplay">Cola: []</p>

    <script>
        // LIFO (Pila)
        let stack = [];

        function pushToStack() {
            let item = prompt("Introduce un elemento para la pila:");
            if (item) {
                stack.push(item); // Agrega el elemento al final de la pila
                displayStack();
            }
        }

        function popFromStack() {
            if (stack.length > 0) {
                let removedItem = stack.pop(); // Elimina el último elemento agregado
                alert("Elemento removido de la pila: " + removedItem);
                displayStack();
            } else {
                alert("La pila está vacía");
            }
        }

        function displayStack() {
            document.getElementById("stackDisplay").innerText = "Pila: [" + stack.join(", ") + "]";
        }

        // FIFO (Cola)
        let queue = [];

        function enqueueToQueue() {
            let item = prompt("Introduce un elemento para la cola:");
            if (item) {
                queue.push(item); // Agrega el elemento al final de la cola
                displayQueue();
            }
        }

        function dequeueFromQueue() {
            if (queue.length > 0) {
                let removedItem = queue.shift(); // Elimina el primer elemento de la cola
                alert("Elemento removido de la cola: " + removedItem);
                displayQueue();
            } else {
                alert("La cola está vacía");
            }
        }

        function displayQueue() {
            document.getElementById("queueDisplay").innerText = "Cola: [" + queue.join(", ") + "]";
        }
    </script>
</body>
</html>
