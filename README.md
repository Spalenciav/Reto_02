# Reto-dos

# Juego de mesa quarto o cuarto
El juego de mesa que realicé fue Quarto, un juego que me parece bastante entretenido y estratégico, parecido al ajedrez. Se cuentan con un total de 8 fichas por cada jugador, en un tablero de 4x4. Cada una de las fichas cuenta con características únicas como la altura, la forma, el color o su contenido (si es sólida o hueca). Para ganar, se necesita hacer una línea de 4 fichas con una misma característica. Por ejemplo, un jugador gana si pone la última ficha en una fila de 4 piezas con la característica cuadrada, todas las fichas presentan esta característica y forman un cuarto.
Para empezar, un jugador elige la ficha de su rival, luego el rival elige dónde va a colocar la ficha hasta que se terminen las fichas o se realice el cuarto.

```mermaid
classDiagram
    Cuarto"1" <-- "2"Jugadores
    Cuarto"1" *-- "1"Tablero
    Tablero"1" *-- "16" Posiciones
    Cuarto"1" *-- "16" Piezas 
    Cuarto : +ListaDePiezas
    Cuarto : +Tablero
    Cuarto : 
    class Jugadores{
      +String beakColor
      +JugarTurno()
    }
    class Tablero{
      -JuegoCuarto
      -Posicion
      -Posicionar()
    }
    class Posiciones{
      +JuegoCuarto 
    }
    class Piezas{
      +JuegoCuarto 
    }
```
```mermaid
classDiagram
    Piezas"1" *-- "2" Pieza_1
    Piezas"1" *-- "2" Pieza_2
    Piezas"1" *-- "2" Pieza_3
    Piezas"1" *-- "2" Pieza_4
    Piezas"1" *-- "2" Pieza_5
    Piezas"1" *-- "2" Pieza_6
    Piezas"1" *-- "2" Pieza_7
    Piezas"1" *-- "2" Pieza_8
    class Piezas{
        +JuegoCuarto
+color
    }

    class Pieza_1{
        -Cuadradra
        -Alta 
        -Solida
        -Posicionar()
    }
        class Pieza_2{
        -Cuadrada
        -Alta
        -Hueca
        -Posicionar()
    }
        class Pieza_3{
        -Cuadrada
        -Baja
        -Solida
        -Posicionar()
    }
        class Pieza_4{
        -Cuadrada
        -Baja
        -Hueca
        -Posicionar()
    }
        class Pieza_5{
        -Redonda
        -Alta
        -Solida
        -Posicionar()
    }
        class Pieza_6{
        -Redonda
        -Alta
        -Hueca
        -Posicionar()
    }
        class Pieza_7{
        -Redonda
        -Baja
        -Solida
        -Posicionar()
    }
        class Pieza_8{
        -Redonda
        -Baja
        -Hueca
        -Posicionar()
    }
```

