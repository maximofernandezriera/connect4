# connect4
https://www.codewars.com/kata/586c0909c1923fdb89002031/train/java

# Análisis del problema

* El problema consiste en un tablero de 7 columnas por 6 filas donde dos jugadores colocan discos por turnos. 
* El objetivo es ser el primero en formar una línea de cuatro discos propios, ya sea horizontal, vertical o diagonalmente.
* Implementaremos una clase Connect4 con un método play que recibe la columna donde el jugador desea colocar su disco.
* El juego debe manejar estados como victoria de un jugador, columna llena y finalización del juego, mostrando mensajes específicos en cada caso.

Para abordar esto deberíamos implementar estos pasos:

1. Diseñar la clase Connect4:

- Crear una representación interna del tablero.
- Inicializar el tablero y el estado del juego.
- Alternar entre los jugadores tras cada movimiento válido.

2. Implementar el método play(int column).

- Verificar si la columna está llena y retornar "Column full!" si es el caso.
- Colocar el disco en la posición adecuada.
- Verificar si el movimiento resulta en un ganador.
- Cambiar el turno al siguiente jugador si el juego continúa.

3. Métodos adicionales:

- Verificar el estado del tablero y buscar ganadores.
- Tener en cuenta la lógica de cambio de turnos.

4. Gestión de los estados:

- Mantener el control del jugador actual.
- Mantener el estado de la partida (en juego, ganada, etc.).

# Pseudocódigo

## Attributes of Connect4 class
    
    BoardArray = array[1..ROWS, 1..COLUMNS] of Integer
    board: BoardArray
    currentPlayer: Integer = 1
    gameWon: Boolean = false

## Methods of Connect4 class

    method String Play(column: Integer)

      row: Integer
      
    if gameWon {
      return 'Game has finished!'
      for row := ROWS to 1 do
        if board[row, column] = 0 {
          board[row, column] := currentPlayer
            if CheckWin(row, column) {
              gameWon := true
              return 'Player ' + currentPlayer + ' wins!'
            }
          currentPlayer := 3 - currentPlayer
           return 'Player ' + currentPlayer + ' has a turn'
      }
      return 'Column full!'
    }
    
    method Boolean CheckWin(row, column: Integer)
    {
     Call to CheckHorizontal, CheckVertical, and CheckDiagonal
    }
    
    method Boolean checkHorizontal(int row, int column)
    {
            return true or false
    }
    
    method Boolean checkVertical(int row, int column)
    {
            return true or false
    }
    
    method Boolean checkDiagonal(int row, int column)
    {
            return true or false
    }
