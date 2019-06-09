# Parking lot management using `clojure`
## Problem Statement
I own a parking lot that can hold up to 'n' cars at any given point in time. Each slot is given a number starting at 1 increasing with increasing distance from the entry point in steps of one. I want to create an automated ticketing system that allows my customers to use my parking lot without human intervention.
When a car enters my parking lot, I want to have a ticket issued to the driver. The ticket issuing process includes us documenting the registration number (number plate) and the colour of the car and allocating an available parking slot to the car before actually handing over a ticket to the driver (we assume that our customers are nice enough to always park in the slots allocated to them).
The customer should be allocated a parking slot which is nearest to the entry. At the exit the customer returns the ticket which then marks the slot they were using as being available.
Due to government regulation, the system should provide me with the ability to findout:
● Registration numbers of all cars of a particular colour.
● Slot number in which a car with a given registration number is parked.
● Slot numbers of all slots where a car of a particular colour is parked.
We interact with the system via a simple set of commands which produce a specific output. Please take a look at the example below, which includes all the commands you need to support - they're self explanatory. The system should allow input in two
ways. Just to clarify, the same codebase should support both modes of input - we don't want two distinct submissions.
1) It should provide us with an interactive command prompt based shell where commands can be typed in
2) It should accept a filename as a parameter at the command prompt and read the commands from that file

## `Solution`
## Prerequisites
* Code is designed to work on linux machine.
* Java must be installed.
* [Leiningen](https://leiningen.org/) must be installed.

`NOTE:`_Above code is sucessfully tesetd with Leiningen 2.9.0 on Java 1.8.0_212 OpenJDK 64-Bit Server VM_
### Step 1: Setup
First, Unzip the parking_lot.zip , after that open the terminal and change directory where you unziped it.
Then Write the following command in terminal. It will setup project for you by performing compilation, build and unit testing.
```
parking_lot $ bin/setup
```
### Step 2: Usage
You can run the full suits by 2 modes:
* File mode
* Interactive mode
#### File mode:
Put your `file_inputs.txt` in directory `functional_spec -> fixtures`
```
parking_lot $ bin/parking_lot file_inputs.txt
```
#### Interactive mode:
```
parking_lot $ bin/parking_lot
```
#### APIs Reference
*   (create_parking_lot n)
*  (park reg-no color)
*  (leave i)
*  (status)
*  (slot_numbers_for_cars_with_colour color)
*  (registration_numbers_for_cars_with_colour color)
* (slot_number_for_registration_number reg-no)
# Done
