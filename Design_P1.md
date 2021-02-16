# TicTacToe Player 1 (server) Design
> This is the design document for the TicTacToe Server ([tictactoeP1.c](https://github.com/CSE-5462-Spring-2021/assignment3-conner-n-ben/blob/master/tictactoeP1.c)).  
> By: Conner Graham

## Table of Contents
- TicTacToe Class Protocol - [Protocol Document](https://docs.google.com/document/d/18NELyK0rywzaeZ_eVgDlaO9Z9MJ82zlH7tFRHX5Gh6M/edit?usp=sharing)
- [Environment Constants](#environment-constants)
- [High-Level Architecture](#high-level-architecture)
- [Low-Level Architecturet](#low-level-architecture)

## Environment Constants
```C#
NUM_ARGS = 2      // number of command line arguments
BACKLOG_MAX = 5   // max length for queue of pending connections
ROWS = 3          // number of rows for the TicIacToe board
COLUMNS = 3       // number of columns for the TicIacToe board
```

## High-Level Architecture
At a high level, the server application attempts to validate and extract the arguments passed
to the application. It then attempts to create and bind the server endpoint. If everything was
successful, it then starts listening for clients and waits to connect to another player. If
another player connects, the server initializes the game board and begins the TicTacToe game.
After the game is over, the server closes the connection to the other player. If an error occurs
before the connection is established, the program terminates and prints appropriate error
messages, otherwise an error message is printed and the connection is terminated.
```C
int main(int argc, char *argv[]) {
    TODO
    return 0;
}
```

## Low-Level Architecture
Extracts the user provided arguments to their respective local variables and performs
validation on their formatting. If any errors are found, the function terminates the process.
```C
void extractArgs(params...) {
    /* extract and validate remote port number */
    if (!valid) exit(EXIT_FAILURE);
}
```
Creates the comminication endpoint with the provided IP address and port number. If any
errors are found, the function terminates the process.
```C
int create_endpoint(params...) {
    /* attempt to create socket */
    if (created) {
        /* initialize socket with params from user */
    } else {
        exit(EXIT_FAILURE);
    }
    /* attempt to bind socket to address */
    if (!bind) {
        exit(EXIT_FAILURE);
    }
    return socket-descriptor;
}
```
TODO Note: This function was created by Dr. Ogle (not myself), but I made significant changes to it's
structure so I have included it in my design.
```C
void tictactoe(params...) {
    TODO
}
```
- TODO
    ```C
    int get_player_choice(params...) {
        TODO
    }
    ```
- TODO
    ```C
    int validate_choice(params...) {
        TODO
    }
    ```
