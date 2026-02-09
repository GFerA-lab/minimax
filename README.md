# 🐱🐭 Juego de Gato y Ratón con Minimax

Proyecto de simulación de un **juego de Gato y Ratón** en un laberinto 2D, donde el jugador controla al ratón y la computadora controla al gato utilizando el **algoritmo Minimax** para tomar decisiones óptimas de movimiento.

El objetivo del ratón es **llegar a la salida sin ser atrapado**, mientras que el gato intenta **alcanzar al ratón minimizando la distancia entre ambos**.

---

## 🎯 Objetivos del Proyecto

- Aplicar el algoritmo **Minimax** en un entorno discreto.
- Simular toma de decisiones en juegos por turnos.
- Representar un entorno mediante matrices.
- Practicar búsqueda de caminos y evaluación de estados.
- Implementar interacción por consola.

---

## 🧩 Descripción General

El juego se desarrolla sobre un laberinto representado como una matriz 2D.  
Cada turno consiste en:

1. El jugador mueve al ratón usando el teclado.
2. El gato calcula su mejor movimiento usando **Minimax** con profundidad limitada.
3. Se actualiza el estado del tablero.
4. Se verifica si hay condiciones de victoria o derrota.

El laberinto se muestra en consola utilizando **emojis** para facilitar la visualización.

---

## 🗺️ Representación del Laberinto

La matriz del laberinto utiliza los siguientes valores:

| Valor | Significado |
|------|------------|
| `0` | Camino libre |
| `1` | Pared |
| `2` | Ratón 🐭 |
| `3` | Gato 🐱 |
| `4` | Salida 🚪 |
| `5` | Gato triste (ratón gana) 😿 |
| `6` | Gato feliz (gato gana) 😼 |

---

## 🎮 Controles

El jugador controla al ratón con las siguientes teclas:

| Tecla | Movimiento |
|------|-----------|
| `W` | Arriba |
| `S` | Abajo |
| `A` | Izquierda |
| `D` | Derecha |

Los movimientos inválidos (paredes o límites del mapa) son rechazados.

---

## 🧠 Algoritmo Minimax

El gato utiliza el algoritmo **Minimax** para decidir su movimiento:

- **Gato (Minimizador):** intenta reducir la distancia hacia el ratón.
- **Ratón (Maximizador):** intenta aumentar su distancia respecto al gato.
- La profundidad del árbol de búsqueda es limitada para evitar un costo computacional alto.

La evaluación de cada estado se basa en la **cantidad de pasos necesarios para alcanzar al oponente**, calculada mediante una búsqueda recursiva en el laberinto.

---

## 🔍 Funciones Principales

### `buscar_objetivo`
Calcula la distancia aproximada entre dos posiciones del laberinto utilizando búsqueda recursiva y backtracking.

### `get_valid_moves`
Devuelve los movimientos válidos desde una posición dada, evitando paredes y límites del tablero.

### `movimiento`
Implementa el algoritmo Minimax y devuelve:
- El valor de evaluación del estado.
- El mejor movimiento posible para el jugador actual.

### `validar_direccion`
Verifica si el movimiento ingresado por el jugador es válido y retorna la nueva posición.

### `mostrar`
Imprime el laberinto en consola utilizando emojis para representar cada elemento del juego.

---

## 🏁 Condiciones de Finalización

El juego termina cuando:

- 🐱 **El gato atrapa al ratón** → gana el gato.
- 🐭 **El ratón llega a la salida** → gana el ratón.

En ambos casos, se muestra el estado final del laberinto.

---

## ▶️ Ejecución

1. Asegurarse de tener **Python 3** instalado.
2. Clonar el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/gato-raton-minimax.git
