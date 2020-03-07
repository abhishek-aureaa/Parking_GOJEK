1. Assumption - Ubuntu 18 is used , Though it should work on Ubuntu 16 or 14 as well(not tested though) & may be even older Ubuntu Version than 14.
2. In the project root folder run : chmod +x bin/setup
3. In the project root folder run : chmod +x bin/parking_lot 
4. To install all dependencies, compile and run unit tests, In the project root folder run :  bin/setup 
5. To run the program so that it accepts input from a file, In the project root folder run :  bin/parking_lot file_inputs.txt 

6. To run the program and launch the shell in interactive mode , In the project folder run :  bin/parking_lot
Example : 
-------------------------------------------
$ bin/parking_lot
Please enter 'exit' to quit
Waiting for input...


Input:
create_parking_lot 6
Expected Output:
Created a parking lot with 6 slots

Input:
park KA-01-HH-1234 White
Expected Output:
Allocated slot number: 1

Input:
park KA-01-HH-9999 White
Expected Output:
Allocated slot number: 2

Input:
park KA-01-BB-0001 Black
Expected Output:
Allocated slot number: 3

Input:
park KA-01-HH-7777 Red
Expected Output:
Allocated slot number: 4

Input:
park KA-01-HH-2701 Blue
Expected Output:
Allocated slot number: 5

Input:
park KA-01-HH-3141 Black
Expected Output:
Allocated slot number: 6

Input:
leave 4
Expected Output:
Slot number 4 is free

Input:
status
Expected Output:
Slot No. Registration No Color
1 KA-01-HH-1234 White
2 KA-01-HH-9999 White
3 KA-01-BB-0001 Black
5 KA-01-HH-2701 Blue
6 KA-01-HH-3141 Black

Input:
park KA­01­P­333 White
Expected Output:
Allocated slot number: 4

Input:
park DL­12­AA­9999 White
Expected Output:
Sorry, parking lot is full

Input:
registration_numbers_for_cars_with_colour White
Expected Output:
KA-01-HH-1234, KA-01-HH-9999, KA-01-P-333

Input:
slot_numbers_for_cars_with_colour White
Expected Output:
1, 2, 4

Input:
slot_number_for_registration_number KA-01-HH-3141
Expected Output:
6

Input:
slot_number_for_registration_number MH-04-AY-1111
Expected Output:
Not found

exit
-------------------------------------------

7. To Run Unit Test, In the project folder run : mvn clean test
