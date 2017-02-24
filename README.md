# MIS40750AirlineSeating
Module : Analytics Research And Implementation
Name : Sharon Luk
Student Number : 16203615

1. Algorithm Implementation
The algorithm involves a recursive function to find the best positions for the passenger to book.
Given a table with 10 columns and 8 rows in which T represents the seat is taken, C represents column and R
represents row.

The first scenario : 
The output would be the following if the flight passenger books 7 seats : 

   C1 C2 C3 C4 C5 C6 C7 C8 C9 C10
R1 T1 T1 T1 T1 T1 T1 T1 
R2
R3
R4
R5
R6
R7
R8

The second scenario:
If a second passenger decides to book 5 seats, the output would be the following :

   C1 C2 C3 C4 C5 C6 C7 C8 C9 C10
R1 T1 T1 T1 T1 T1 T1 T1 T2 T2 T2
R2                         T2 T2
R3
R4
R5
R6
R7
R8

The third scenario:
It can also create seperate passenger group bookings if there are not enough empty seat positions :

   C1 C2 C3 C4 C5 C6 C7 C8 C9 C10
R1 T1 T1 T1 T1 T1 T1 T1 T2 T2 T2
R2 Ti Ti Ti Ti Ti       Ti T2 T2
R3 Ti Ti Ti Ti Ti       Ti Ti Ti
R4 Ti Ti Ti Ti Ti Ti Ti Ti Ti Ti
R5 Ti          Ti Ti Ti Ti Ti Ti
R6 Ti Ti Ti Ti Ti Ti Ti Ti Ti Ti
R7 Ti Ti Ti Ti Ti Ti Ti Ti Ti Ti
R8 Ti Ti Ti Ti Ti Ti Ti Ti

The fourth scenario:
If the third passenger decided to book 7 seats, firstly the 4 seats would be found and then the remaining 3 seats
available followed by another seat :

   C1 C2 C3 C4 C5 C6 C7 C8 C9 C10
R1 T1 T1 T1 T1 T1 T1 T1 T2 T2 T2
R2 Ti Ti Ti Ti Ti T3 T3 Ti T2 T2
R3 Ti Ti Ti Ti Ti T3 T3 Ti Ti Ti
R4 Ti Ti Ti Ti Ti Ti Ti Ti Ti Ti
R5 Ti T3 T3 T3 Ti Ti Ti Ti Ti Ti
R6 Ti Ti Ti Ti Ti Ti Ti Ti Ti Ti
R7 Ti Ti Ti Ti Ti Ti Ti Ti Ti Ti
R8 Ti Ti Ti Ti Ti Ti Ti Ti T3

At this point, if a another passenger decides to book more than one seat eg 5 seats. The seat allocation will fail
as there is only one seat remaining.

The recursive function finds the positions of north,south, east and west to book seats accordingly as a whole.
In the cases of not having enough empty seats to book the group of passengers, the recursive function will create
seperated groups.
