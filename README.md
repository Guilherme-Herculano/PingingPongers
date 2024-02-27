# PingingPongers

This repository demonstrates concurrent programming in Go using channels. It features two functions, "ping" and "pong", that send messages to a channel, and a "print" function that receives and prints the messages to the screen. This creates a simple simulation of a production line where messages are alternately produced and displayed.

## Getting Started

To get started, clone the repository and run the following commands:

go mod download.
go run main.go.
This will start the program and you should see "Ping" and "Pong" messages alternately printed to the screen.

## How it works

The program consists of three main functions:

ping(): This function continuously sends the message "Ping" to the channel c.
pong(): This function continuously sends the message "Pong" to the channel c.
print(): This function receives messages from the channel c and prints them to the screen.
The main() function creates the channel c and then starts the three functions as goroutines. A goroutine is a lightweight thread of execution in Go.

The print() function uses the <- operator to receive messages from the channel c. The <- operator blocks until a message is available on the channel.

The ping() and pong() functions use the -> operator to send messages to the channel c. The -> operator sends the message to the channel and then returns immediately.

## Concepts demonstrated

This project demonstrates the following concepts:

Concurrency: The ability to run multiple tasks at the same time.
Channels: A way to communicate between goroutines.
Goroutines: Lightweight threads of execution in Go.
