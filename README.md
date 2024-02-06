# connect4
https://www.codewars.com/kata/586c0909c1923fdb89002031/train/java

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
