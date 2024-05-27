# Breakout Game MOO ICT - Detailed Description

## Descripción de la Aplicación

La aplicación es un juego de Breakout desarrollado en C# utilizando Windows Forms. El objetivo del juego es controlar una barra para hacer rebotar una pelota y romper bloques dispuestos en la parte superior de la ventana. 

## Estructura del Código

### Clases

#### `Form1`

La clase principal de la aplicación que hereda de `Form`. Esta clase contiene la lógica principal del juego, incluyendo la inicialización de componentes, manejo de eventos, y la lógica del juego.

### Variables

#### `bool goLeft`

Indica si la barra del jugador se está moviendo hacia la izquierda.

#### `bool goRight`

Indica si la barra del jugador se está moviendo hacia la derecha.

#### `bool isGameOver`

Indica si el juego ha terminado.

#### `int score`

Lleva la cuenta del puntaje del jugador.

#### `int ballx`

Velocidad horizontal de la pelota.

#### `int bally`

Velocidad vertical de la pelota.

#### `int playerSpeed`

Velocidad de movimiento de la barra del jugador.

#### `Random rnd`

Generador de números aleatorios utilizado para asignar colores a los bloques y la dirección de la pelota.

#### `PictureBox[] blockArray`

Arreglo que contiene los bloques del juego.

### Métodos

#### `public Form1()`

Constructor de la clase `Form1`. Inicializa los componentes y coloca los bloques llamando al método `PlaceBlocks()`.

#### `private void setupGame()`

Configura el estado inicial del juego. Reinicia variables, posiciona la pelota y la barra del jugador, y asigna colores aleatorios a los bloques.

#### `private void gameOver(string message)`

Finaliza el juego. Detiene el temporizador del juego y muestra un mensaje con el puntaje final.

#### `private void PlaceBlocks()`

Crea y posiciona los bloques en la ventana del juego. Inicializa el arreglo `blockArray` y asigna colores y posiciones a cada bloque.

#### `private void removeBlocks()`

Elimina todos los bloques de la ventana del juego.

#### `private void mainGameTimerEvent(object sender, EventArgs e)`

Evento principal del juego que se ejecuta en cada tick del temporizador. Maneja el movimiento de la pelota y la barra del jugador, y detecta colisiones con los bloques y las paredes.

#### `private void keyisdown(object sender, KeyEventArgs e)`

Maneja el evento de presionar una tecla. Si se presiona la tecla izquierda o derecha, actualiza las variables `goLeft` o `goRight` respectivamente.

#### `private void keyisup(object sender, KeyEventArgs e)`

Maneja el evento de soltar una tecla. Si se suelta la tecla izquierda o derecha, actualiza las variables `goLeft` o `goRight` respectivamente. Si se presiona la tecla Enter y el juego ha terminado, reinicia el juego.

#### `private void Form1_Load(object sender, EventArgs e)`

Método de carga del formulario, que se ejecuta cuando el formulario se carga por primera vez. Actualmente no realiza ninguna acción.

## Imágenes de la Aplicación

### Pantalla Inicial
![Pantalla Inicial](https://github.com/Marlon-Trujillo-Jaramillo/Breakout-Game-/blob/master/Captura%20de%20pantalla%202024-05-20%20121419.png)

### Durante el Juego
![Durante el Juego](https://github.com/Marlon-Trujillo-Jaramillo/Breakout-Game-/blob/master/Captura%20de%20pantalla%202024-05-20%20121441.png)

### Juego Terminado
![Juego Terminado](https://github.com/Marlon-Trujillo-Jaramillo/Breakout-Game-/blob/master/Captura%20de%20pantalla%202024-05-20%20121530.png)
